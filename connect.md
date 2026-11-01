<!---
ICON=fa-solid fa-server
ROUTE=connect
SHORT=Connect
TITLE=Connect to osu!Destiny
NAVBAR=true
FOOTER=false
BEHINDLOGIN=false
-->
### How to connect

1. Create an osu! shortcut (right-click `osu!.exe` → Send to → Desktop, or copy the existing shortcut).
2. Right-click the shortcut and select **Properties**.
3. In the **Target** field, after the path to osu!, add the devserver flag:

<input class="form-control" type="readonly" id="dev" value=" -devserver osudestiny.xyz"></input>

<a class="btn btn-info" onclick="copydev()">Copy devserver</a>

4. Launch osu! from that shortcut, then **register in-game or on the website** with a new username and password.

> Note: if osu! runs a "force repair", it relaunches in updater mode and drops the `-devserver` flag (sending you back to official osu!). Just start again from your shortcut.

<script>
    function copydev() {
        var copyText = document.getElementById("dev");
        copyText.select();
        copyText.setSelectionRange(0, 99999);
        navigator.clipboard.writeText(copyText.value);
        alert("Copied: " + copyText.value);
    }
</script>
