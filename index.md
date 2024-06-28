<!-- centering markdown images -->
<p align="center">
  <img src="images/MedHackathon_logo.png">
</p>

# MedHackathon 2025

<select id="language">
  <option value="sq">Albanian</option>
  <option value="ar">Arabic</option>
  <option value="az">Azerbaijani</option>
  <option value="bn">Bengali</option>
  <option value="bg">Bulgarian</option>
  <option value="ca">Catalan</option>
  <option value="zh">Chinese</option>
  <option value="zh-TW">Chinese (traditional)</option>
  <option value="cs">Czech</option>
  <option value="da">Danish</option>
  <option value="nl">Dutch</option>
  <option value="en">English</option>
  <option value="eo">Esperanto</option>
  <option value="et">Estonian</option>
  <option value="fi">Finnish</option>
  <option value="fr">French</option>
  <option value="de">German</option>
  <option value="el">Greek</option>
  <option value="he">Hebrew</option>
  <option value="hi">Hindi</option>
  <option value="hu">Hungarian</option>
  <option value="id">Indonesian</option>
  <option value="ga">Irish</option>
  <option value="it">Italian</option>
  <option value="ja">Japanese</option>
  <option value="ko">Korean</option>
  <option value="lv">Latvian</option>
  <option value="lt">Lithuanian</option>
  <option value="ms">Malay</option>
  <option value="no">Norwegian</option>
  <option value="fa">Persian</option>
  <option value="pl">Polish</option>
  <option value="pt">Portuguese</option>
  <option value="ro">Romanian</option>
  <option value="ru">Russian</option>
  <option value="sr">Serbian</option>
  <option value="sk">Slovak</option>
  <option value="sl">Slovenian</option>
  <option value="es">Spanish</option>
  <option value="sv">Swedish</option>
  <option value="tl">Tagalog</option>
  <option value="th">Thai</option>
  <option value="tr">Turkish</option>
  <option value="uk">Ukrainian</option>
  <option value="ur">Urdu</option>
  <option value="vi">Vietnamese</option>
</select>
<button onclick="translateText()">Translate</button>

<script>
async function translateText() {
  const text = document.getElementById('content').innerText;
  const language = document.getElementById('language').value;

  const response = await fetch('https://libretranslate.com/translate', {
    method: 'POST',
    body: JSON.stringify({
      q: text,
      source: 'jp',
      target: language,
      format: 'text'
    }),
    headers: { 'Content-Type': 'application/json' }
  });

  const data = await response.json();
  document.getElementById('content').innerText = data.translatedText;
}
</script>

<container id="content">

## Background

The diversity in Asian genomic data holds immense potential to enhance our understanding of human genetics globally. However, there is currently a lack of communication and collaboration among national genome projects in various Asian countries. This fragmentation undermines the potential benefits that each country's unique efforts and resources can bring to the field of medical informatics. By fostering better communication and collaboration, we can raise the value and impact of individual national projects, ultimately contributing to a more comprehensive and inclusive understanding of human genetics.

## Objectives

The primary objective of the MedHackathon is to establish a robust networking platform for medical informatics researchers across Asia. By bringing together experts from diverse backgrounds, the event aims to foster collaboration and facilitate the exchange of knowledge and experiences. This collective effort is intended to build a cohesive community that respects and values the unique contributions of each country. Through enhanced networking, the event seeks to bridge the existing communication gaps and create a unified approach to advancing medical informatics research in the region.

## Tentative Schedule

3-7 February 2025

## Tentative place

Buri, Chonburi, Thailand

</container>

<script>
document.addEventListener("DOMContentLoaded", function() {
    // Select the specific <h1> element with the <a> tag containing the link to "https://medhackathon.github.io/2025/"
    var elementToRemove = document.querySelector('h1 a[href="https://medhackathon.github.io/2025/"]');
    if (elementToRemove) {
        var parent = elementToRemove.closest('h1'); // Find the closest <h1> ancestor
        if (parent) {
            parent.remove(); // Remove the <h1> element
        }
    }
});
</script>
