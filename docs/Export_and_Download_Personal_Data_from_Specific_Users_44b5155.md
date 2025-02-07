<!-- copy44b5155cc34249da8f3efb216d3e2f88 -->

# Export and Download Personal Data from Specific Users

You can export and download personal data from specific users from your workspace.

1.  In your browser, get a list of all workspaces contained in a specific subaccount:

    ```
    https://<sap-business-application-studio-url>/ws-manager/api/v1/workspace?all=true
    ```

2.  Enter your administrator credentials in the login page.
3.  From the list provided, identify the dev space you want to export \(for example by searching for the username property\).
4.  Copy the `url` property under the `runtime` section and remove `-theia/` from the URL. This URL is the `<runtime-url>` parameter used in the request below.
5.  Make sure the dev space you want to export is in status *Running*. If not, wake up the dev space before exporting the data. See, [Restart a Dev Space](Restart_a_Dev_Space_1f54583.md)
6.  Use the following request to export data:

    ```
    https://<sap-business-application-studio-url>/login?e=<runtime-url>/wsmaintain/export
    ```


