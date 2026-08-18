# 海外の飲食チェーンに関するアンケート

Static survey page for a PureSpectrum Marketplace field. Panel respondents
arrive with a respondent id on the query string; the page screens, collects
three questions, posts results to a Google Apps Script collector, and
redirects back to the panel with the id intact.

Config lives in the `CFG` block near the top of the `<script>` in `index.html`.

- `ENDPOINT`      — Apps Script web app `/exec` URL
- `PID_PARAM`     — inbound query param carrying the respondent id
- `COMPLETE_URL`  — PureSpectrum complete redirect (keep the `{PID}` token)
- `TERMINATE_URL` — PureSpectrum screenout redirect (keep the `{PID}` token)

Set `REQUIRE_PID` to `false` only for local testing.
