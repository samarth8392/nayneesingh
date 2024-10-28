---
layout: page
title: ""
subtitle: Download a copy of my resume
use-site-title: true
css : "assets/css/pdf.css"
---

<p align="center"> <i> Last Updated: 08/26/24 </i> </p>

<script src="../assets/js/pdfobject.min.js"></script>

<div class="pdf-container">
    <div id="pdf" class="pdf-viewer"></div>
</div>

<script>
    // Check if mobile device
    const isMobile = /iPhone|iPad|iPod|Android/i.test(navigator.userAgent);
    
    if (isMobile) {
        // For mobile devices, use Google Docs Viewer as fallback
        const pdfUrl = encodeURIComponent("https://github.com/samarth8392/nayneesingh/blob/master/Naynee_Singh_CV_PDF.pdf");
        document.getElementById('pdf').innerHTML = `
            <iframe src="https://docs.google.com/viewer?url=${pdfUrl}&embedded=true" 
                    width="100%" 
                    height="100%" 
                    style="border: none;">
            </iframe>`;
    } else {
        // For desktop, use PDFObject
        PDFObject.embed("../Naynee_Singh_CV_PDF.pdf", "#pdf", {
            fallbackLink: "<p>This browser does not support inline PDFs. <a href='../Naynee_Singh_CV_PDF.pdf'>Click here to download the PDF</a>.</p>",
            height: "100%",
            width: "100%"
        });
    }
</script>

<!-- 

<div id="pdf" style="height: 800px;"></div>
<script src="../assets/js/pdfobject.min.js"></script>
<script>
PDFObject.embed("../Naynee_Singh_CV_PDF.pdf", "#pdf");
</script> -->
