
2. Then add the JavaScript functions before the closing body tag:


```diff
<<<<<<< SEARCH
    </script>
<footer style="margin-top: 30px; text-align: center; padding: 20px; font-size: 0.9em; color: #666;">
=======
    </script>
    <script>
        function downloadPDF() {
            alert('To generate PDF: Right click anywhere on page → Print → Save as PDF\nOr Ctrl+P → Save as PDF');
        }
        
        function downloadMarkdown() {
            const title = document.title;
            const mdContent = `# ${title}\n\n`;
            const blob = new Blob([mdContent], {type: 'text/markdown'});
            const url = URL.createObjectURL(blob);
            const a = document.createElement('a');
            a.href = url;
            a.download = 'email-sender-readme.md';
            document.body.appendChild(a);
            a.click();
            document.body.removeChild(a);
        }
    </script>
    <footer style="margin-top: 30px; text-align: center; padding: 20px; font-size: 0.9em; color: #666;">
>>>>>>> REPLACE
