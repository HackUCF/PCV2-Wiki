# Troubleshooting

This page provides methods for troubleshooting problems the end user may run into.

## Hackucf DNS records not resolving:
   <details>
      <summary>Fix for Custom DNS Users</summary><br>
      <span>If you run your own local DNS and you cannot resolve horizon.hackucf.cloud with nslookup, then you will need to add the following to your Records.</span></br></br>
      <span>DNS Records:</span>
      <table>
         <tr>
            <th>Domain</th>
            <th>IP Address</th>
         </tr>
         <tr>
            <td>cloud.hackucf</td>
            <td>10.4.4.10</td>
         </tr>
      </table>
      <span>CNAME Records:</span>
      <table>
         <tr>
            <th>FQDN</th>
            <th>Domain</th>
         </tr>
         <tr>
            <td>horizon.hackucf.cloud</td>
            <td>cloud.hackucf</td>
         </tr>
         <tr>
            <td>api.hackucf.cloud</td>
            <td>cloud.hackucf</td>
         </tr>
      </table>
   </details>