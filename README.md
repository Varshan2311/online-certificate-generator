<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Trending Attractive Certificate</title>
<link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@700&family=Open+Sans&display=swap" rel="stylesheet" />
<style>
body {
font-family: 'Open Sans', sans-serif;
background: #f9f6f1;
margin: 0;
display: flex;
flex-direction: column;
align-items: center;
padding: 30px 20px;
color: #5c3a12;
}
h1 {
font-family: 'Montserrat', sans-serif;
font-weight: 700;
color: #a76d3b;
font-size: 36px;
margin-bottom: 24px;
}
.form-container {
width: 420px;
background: #fff8e1;
border-radius: 15px;
padding: 25px 30px;
box-shadow: 0 12px 24px rgba(167,109,59,0.25);
margin-bottom: 30px;
}
label, input, select {
width: 100%;
display: block;
margin: 14px 0 8px 0;
font-size: 16px;
}
input, select {
padding: 10px 14px;
border: 2px solid #d4af37;
border-radius: 8px;
font-size: 16px;
box-sizing: border-box;
font-family: 'Open Sans', sans-serif;
}
input:focus, select:focus {
border-color: #a76d3b;
outline: none;
}
button {
appearance: none;
font-family: 'Montserrat', sans-serif;
font-weight: 700;
background-color: #a76d3b;
color: white;
border: none;
border-radius: 10px;
padding: 14px 26px;
margin: 10px 10px 0 0;
cursor: pointer;
font-size: 16px;
transition: background-color 0.3s ease;
}
button:hover {
background-color: #7b4e21;
}
#certificate {
position: relative;
width: 900px;
max-width: 100%;
background: linear-gradient(145deg, #fffbe6, #f5efd5);
border-radius: 26px;
box-shadow: 0 15px 40px rgba(113, 74, 27, 0.2);
padding: 60px 80px 50px 80px;
box-sizing: border-box;
display: none;
}
.badge {
position: absolute;
top: 30px;
left: 30px;
background: #f0c14b;
border-radius: 50%;
width: 46px;
height: 46px;
display: flex;
justify-content: center;
align-items: center;
box-shadow: 0 3px 8px rgba(213, 163, 63, 0.6);
cursor: default;
}
.badge svg {
width: 22px;
height: 22px;
fill: #fff8c6;
filter: drop-shadow(0 0 1px #ceb96e);
}
h2.title {
font-family: 'Montserrat', sans-serif;
font-weight: 700;
font-size: 38px;
letter-spacing: 1.1px;
text-align: center;
margin-bottom: 20px;
color: #7a4e10;
}
.certificate-text {
font-size: 21px;
text-align: center;
line-height: 1.5;
color: #5c3a12;
}
.recipient {
font-family: 'Montserrat', sans-serif;
font-weight: 700;
font-size: 36px;
margin: 24px 0 18px 0;
letter-spacing: 1.4px;
color: #9c6c1b;
}
.course {
font-weight: 600;
font-size: 24px;
margin-bottom: 26px;
color: #7a4e10;
}
.date {
font-style: italic;
font-size: 18px;
color: #725a2a;
margin-bottom: 48px;
}
.signature-line {
height: 3px;
border-radius: 22px;
width: 280px;
margin: 0 auto 12px auto;
background: linear-gradient(90deg, #a97e33, #cfac4c);
box-shadow: 0 2px 4px #b38621;
}
.signature-text {
font-size: 16px;
text-align: center;
letter-spacing: 0.5px;
color: #8d6f3b;
margin-bottom: 40px;
}
.cert-id {
font-size: 17px;
position: absolute;
left: 60px;
bottom: 48px;
color: #826b36;
font-weight: 600;
letter-spacing: 0.6px;
}
#qrcode {
position: absolute;
bottom: 48px;
right: 60px;
width: 80px;
height: 80px;
}
.share-buttons {
width: 900px;
max-width: 100%;
margin-top: 30px;
text-align: center;
}
.share-buttons button {
font-family: 'Montserrat', sans-serif;
padding: 14px 26px;
border: none;
border-radius: 25px;
background: #a76d3b;
color: white;
font-weight: 700;
margin: 0 12px;
cursor: pointer;
transition: background-color 0.3s ease;
box-shadow: 0 8px 12px rgba(167,109,59,0.6);
}
.share-buttons button:hover {
background: #744a05;
}
</style>
</head>
<body>
<h1>Online Certification Generator</h1>
<div class="form-container">
<label for="name">Recipient Name</label>
<input type="text" id="name" placeholder="Enter your full name" />
<label for="course">Course Name</label>
<input type="text" id="course" placeholder="E.g., Python Fundamentals" />
<label for="date">Completion Date</label>
<input type="date" id="date" />
<button onclick="generateCertificate()">Generate Certificate</button>
<button onclick="downloadCertificate()">Download Certificate</button>
</div>
<div id="certificate">
<div class="badge" title="Certificate Badge" aria-label="Certificate Badge">
<svg viewBox="0 0 24 24" aria-hidden="true">
<circle cx="12" cy="12" r="12"/>
<polygon points="12,5 13.9,10 19,10.5 15,13.8 16.5,19 12,16 7.5,19 9,13.8 5,10.5 10.1,10" />
</svg>
</div>
<h2 class="title">Certificate of Completion</h2>
<div class="certificate-text">
<p>This is to certify that</p>
<div class="recipient" id="certName"></div>
<p>has successfully completed the</p>
<div class="course" id="certCourse"></div>
<p class="date" id="certDate"></p>
</div>
<div class="signature-line"></div>
<div class="signature-text">Authorized Signature</div>
<div class="cert-id" id="certId"></div>
<div id="qrcode"></div>
</div>
<div class="share-buttons" style="display:none;">
<button onclick="shareWhatsApp()">Share on WhatsApp</button>
<button onclick="shareLinkedIn()">Share on LinkedIn</button>
</div>

<script src="https://cdn.jsdelivr.net/npm/qrcode/build/qrcode.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/html2canvas@1.4.1/dist/html2canvas.min.js"></script>
<script>
const certificateDiv = document.getElementById('certificate');
const shareButtons = document.querySelector('.share-buttons');
const certName = document.getElementById('certName');
const certCourse = document.getElementById('certCourse');
const certDate = document.getElementById('certDate');
const certId = document.getElementById('certId');
const qrcodeDiv = document.getElementById('qrcode');
let currentCertId = "";

function generateUniqueId() {
  return 'CERT-' + Math.random().toString(36).slice(2, 10).toUpperCase();
}

function generateCertificate() {
  const name = document.getElementById('name').value.trim();
  const course = document.getElementById('course').value.trim();
  const dateVal = document.getElementById('date').value;

  if (!name || !course || !dateVal) {
    alert("Please fill in all details");
    return;
  }

  certName.textContent = name;
  certCourse.textContent = course;
  certDate.textContent = "Date: " + new Date(dateVal).toLocaleDateString();
  currentCertId = generateUniqueId();
  certId.textContent = "Certificate ID: " + currentCertId;

  const verificationUrl = "https://your-organization.com/verify?certId=" + currentCertId;

  qrcodeDiv.innerHTML = "";
  QRCode.toCanvas(qrcodeDiv, verificationUrl, {
    width: 80,
    margin: 1,
    color: { dark: '#5c3a12', light: '#fff0' }
  });

  certificateDiv.style.display = 'block';
  shareButtons.style.display = 'block';
}

// Download certificate as JPG using html2canvas
function downloadCertificate() {
  if (certificateDiv.style.display === 'none') {
    alert("Please generate the certificate first.");
    return;
  }
  html2canvas(certificateDiv).then(canvas => {
    const link = document.createElement('a');
    link.download = currentCertId + ".jpg";
    link.href = canvas.toDataURL("image/jpeg", 1.0); // JPEG format with full quality
    document.body.appendChild(link);
    link.click();
    document.body.removeChild(link);
  }).catch(err => {
    alert("Failed to download certificate. Please try again.");
    console.error(err);
  });
}

function shareWhatsApp() {
  if (!currentCertId) {
    alert("Generate the certificate first.");
    return;
  }
  const shareUrl = encodeURIComponent("https://your-organization.com/verify?certId=" + currentCertId);
  const text = encodeURIComponent("Check out my certificate:");
  window.open(`https://api.whatsapp.com/send?text=${text}%20${shareUrl}`, "_blank");
}

function shareLinkedIn() {
  if (!currentCertId) {
    alert("Generate the certificate first.");
    return;
  }
  const shareUrl = encodeURIComponent("https://your-organization.com/verify?certId=" + currentCertId);
  window.open(`https://www.linkedin.com/sharing/share-offsite/?url=${shareUrl}`, "_blank");
}
</script>
</body>
</html>
