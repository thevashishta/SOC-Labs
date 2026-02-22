# Failed Login Attempt Detection (Windows Log Analysis)

## Objective
To detect repeated authentication failures that may indicate brute-force activity.

## Environment
- Windows 10/11
- Event Viewer
- Security Log Monitoring

## Methodology
1. Generated multiple incorrect password attempts on Windows login screen.
2. Accessed Event Viewer → Windows Logs → Security.
3. Filtered logs using Event ID: 4625 (Failed Logon).
4. Analysed log details including:
   - Target User Name
   - Failure Reason
   - Logon Type
   - Time of attempts

## Observations
- Multiple failed authentication attempts recorded within a short time period.
- Same account targeted repeatedly.
- Failure reason indicated incorrect credentials.
- Log entries confirmed Event ID 4625 (An account failed to log on).

## Detection Insight
Repeated authentication failures for the same user account within a short interval may indicate brute-force attack attempts.

## Conclusion
Monitoring Windows Security logs (Event ID 4625) enables early detection of suspicious authentication activity and potential brute-force behaviour.
