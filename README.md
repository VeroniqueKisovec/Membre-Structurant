[Questionnaire_MembreStructurant_ClubKorvell.html](https://github.com/user-attachments/files/27278753/Questionnaire_MembreStructurant_ClubKorvell.html)
# Membre-Structurant
Formulaire Club Korvell
<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Questionnaire de présentation — Membre Structurant | Club Korvell</title>
<link href="https://fonts.googleapis.com/css2?family=Red+Hat+Display:wght@300;400;500;600;700&family=Red+Hat+Text:wght@300;400;500&display=swap" rel="stylesheet">
<style>
  :root {
    --bleu-fonce: #005277;
    --bleu-moyen: #286682;
    --bleu-clair: #EEF4F7;
    --bleu-accent: #D6E8F0;
    --brun: #46372A;
    --beige: #F9F5F4;
    --beige-moyen: #EEE7E0;
    --sable: #CBAF92;
    --terracotta: #C0805D;
  }

  * { box-sizing: border-box; margin: 0; padding: 0; }

  body {
    font-family: 'Red Hat Text', sans-serif;
    background-color: var(--bleu-clair);
    color: var(--brun);
    min-height: 100vh;
  }

  body::before {
    content: '';
    position: fixed;
    top: 0; right: 0;
    width: 340px;
    height: 100vh;
    background-image: repeating-linear-gradient(
      45deg, transparent, transparent 8px,
      rgba(0,82,119,0.06) 8px, rgba(0,82,119,0.06) 9px
    ),
    repeating-linear-gradient(
      -45deg, transparent, transparent 8px,
      rgba(0,82,119,0.06) 8px, rgba(0,82,119,0.06) 9px
    );
    pointer-events: none;
    z-index: 0;
  }

  header {
    background: var(--bleu-fonce);
    padding: 36px 60px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    position: relative;
    overflow: hidden;
  }

  header::after {
    content: '';
    position: absolute;
    bottom: 0; left: 0; right: 0;
    height: 3px;
    background: linear-gradient(90deg, var(--bleu-moyen), var(--sable), var(--bleu-moyen));
  }

  .header-left h1 {
    font-family: 'Red Hat Display', sans-serif;
    font-size: 13px;
    font-weight: 500;
    letter-spacing: 0.2em;
    color: rgba(255,255,255,0.6);
    text-transform: uppercase;
    margin-bottom: 8px;
  }

  .header-left h2 {
    font-family: 'Red Hat Display', sans-serif;
    font-size: 28px;
    font-weight: 700;
    color: white;
    letter-spacing: 0.03em;
  }

  .badge {
    background: var(--bleu-moyen);
    color: white;
    font-family: 'Red Hat Display', sans-serif;
    font-size: 11px;
    font-weight: 600;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    padding: 8px 18px;
    border-radius: 2px;
    border: 1px solid rgba(255,255,255,0.2);
  }

  .container {
    max-width: 780px;
    margin: 0 auto;
    padding: 60px 40px 80px;
    position: relative;
    z-index: 1;
  }

  .intro {
    background: white;
    border-left: 4px solid var(--bleu-moyen);
    padding: 24px 28px;
    margin-bottom: 50px;
    border-radius: 0 4px 4px 0;
  }

  .intro p {
    font-size: 15px;
    line-height: 1.7;
    color: var(--brun);
  }

  .intro p strong { color: var(--bleu-fonce); }

  .section {
    margin-bottom: 50px;
    opacity: 0;
    transform: translateY(20px);
    animation: fadeUp 0.5s ease forwards;
  }

  .section:nth-child(1) { animation-delay: 0.1s; }
  .section:nth-child(2) { animation-delay: 0.2s; }
  .section:nth-child(3) { animation-delay: 0.3s; }
  .section:nth-child(4) { animation-delay: 0.4s; }
  .section:nth-child(5) { animation-delay: 0.5s; }

  @keyframes fadeUp {
    to { opacity: 1; transform: translateY(0); }
  }

  .section-header {
    display: flex;
    align-items: center;
    gap: 16px;
    margin-bottom: 28px;
    padding-bottom: 14px;
    border-bottom: 1px solid var(--bleu-accent);
  }

  .section-number {
    width: 36px;
    height: 36px;
    background: var(--bleu-fonce);
    color: white;
    font-family: 'Red Hat Display', sans-serif;
    font-weight: 700;
    font-size: 16px;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-shrink: 0;
    border-radius: 2px;
  }

  .section-title {
    font-family: 'Red Hat Display', sans-serif;
    font-size: 16px;
    font-weight: 700;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--bleu-fonce);
  }

  .field-group {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 20px;
    margin-bottom: 20px;
  }

  .field-group.full { grid-template-columns: 1fr; }

  .field {
    display: flex;
    flex-direction: column;
    gap: 8px;
  }

  label {
    font-family: 'Red Hat Display', sans-serif;
    font-size: 12px;
    font-weight: 600;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--bleu-fonce);
  }

  label .required { color: var(--bleu-moyen); margin-left: 3px; }

  input[type="text"],
  input[type="email"],
  input[type="tel"],
  input[type="url"],
  select,
  textarea {
    font-family: 'Red Hat Text', sans-serif;
    font-size: 14px;
    color: var(--brun);
    background: white;
    border: 1px solid var(--bleu-accent);
    border-radius: 3px;
    padding: 12px 16px;
    transition: border-color 0.2s, box-shadow 0.2s;
    outline: none;
    width: 100%;
  }

  input:focus, select:focus, textarea:focus {
    border-color: var(--bleu-moyen);
    box-shadow: 0 0 0 3px rgba(40,102,130,0.12);
  }

  textarea { resize: vertical; min-height: 100px; line-height: 1.6; }

  select {
    appearance: none;
    background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='12' height='8' viewBox='0 0 12 8'%3E%3Cpath d='M1 1l5 5 5-5' stroke='%23005277' stroke-width='1.5' fill='none'/%3E%3C/svg%3E");
    background-repeat: no-repeat;
    background-position: right 14px center;
    padding-right: 40px;
  }

  /* Tags expertise */
  .tags-container {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    margin-bottom: 12px;
  }

  .tag {
    padding: 8px 16px;
    border: 1.5px solid var(--bleu-accent);
    border-radius: 2px;
    font-size: 13px;
    font-weight: 500;
    color: var(--bleu-fonce);
    background: white;
    cursor: pointer;
    transition: all 0.15s;
    user-select: none;
  }

  .tag:hover { border-color: var(--bleu-moyen); background: var(--bleu-clair); }
  .tag.selected { background: var(--bleu-fonce); color: white; border-color: var(--bleu-fonce); }

  /* Upload */
  .upload-zone {
    border: 2px dashed var(--bleu-accent);
    border-radius: 4px;
    padding: 32px 20px;
    text-align: center;
    background: white;
    cursor: pointer;
    transition: all 0.2s;
    position: relative;
  }

  .upload-zone:hover { border-color: var(--bleu-moyen); background: var(--bleu-clair); }

  .upload-zone input[type="file"] {
    position: absolute;
    inset: 0;
    opacity: 0;
    cursor: pointer;
    width: 100%;
    height: 100%;
  }

  .upload-icon { font-size: 28px; margin-bottom: 10px; display: block; }
  .upload-zone p { font-size: 13px; color: var(--brun); font-weight: 500; margin-bottom: 4px; }
  .upload-zone span { font-size: 12px; color: var(--sable); }

  .upload-preview {
    margin-top: 10px;
    font-size: 13px;
    color: var(--bleu-moyen);
    font-weight: 600;
    display: none;
  }

  /* Checkboxes */
  .interests-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 12px;
  }

  .interest-item {
    display: flex;
    align-items: center;
    gap: 12px;
    padding: 14px 16px;
    background: white;
    border: 1px solid var(--bleu-accent);
    border-radius: 3px;
    cursor: pointer;
    transition: all 0.15s;
  }

  .interest-item:hover { border-color: var(--bleu-moyen); background: var(--bleu-clair); }

  .interest-item input[type="checkbox"] {
    accent-color: var(--bleu-fonce);
    width: 16px;
    height: 16px;
    flex-shrink: 0;
  }

  .interest-item input[type="checkbox"]:checked + span { color: var(--bleu-fonce); font-weight: 600; }
  .interest-item.checked { border-color: var(--bleu-moyen); background: var(--bleu-clair); }
  .interest-item span { font-size: 13px; line-height: 1.4; }

  /* Événements */
  .events-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 16px;
  }

  .event-card {
    border-top: 3px solid var(--bleu-moyen);
    background: white;
    padding: 20px 16px;
    border-radius: 0 0 4px 4px;
  }

  .event-card.lancement { border-top-color: var(--bleu-fonce); }

  .event-month {
    font-family: 'Red Hat Display', sans-serif;
    font-weight: 700;
    font-size: 18px;
    color: var(--bleu-moyen);
    margin-bottom: 6px;
  }

  .event-card.lancement .event-month { color: var(--bleu-fonce); }
  .event-label { font-family: 'Red Hat Display', sans-serif; font-size: 12px; font-weight: 600; color: var(--brun); margin-bottom: 8px; }
  .event-desc { font-size: 12px; color: #777; line-height: 1.5; }

  .events-note {
    margin-top: 14px;
    padding: 12px 16px;
    background: var(--bleu-clair);
    border-left: 3px solid var(--bleu-moyen);
    font-size: 13px;
    font-style: italic;
    color: var(--bleu-fonce);
  }

  .submit-area { margin-top: 50px; text-align: center; }

  .submit-btn {
    font-family: 'Red Hat Display', sans-serif;
    font-size: 14px;
    font-weight: 700;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: white;
    background: var(--bleu-fonce);
    border: none;
    padding: 18px 56px;
    border-radius: 3px;
    cursor: pointer;
    transition: all 0.2s;
  }

  .submit-btn:hover {
    background: var(--bleu-moyen);
    transform: translateY(-1px);
    box-shadow: 0 8px 24px rgba(0,82,119,0.3);
  }

  .submit-note { margin-top: 16px; font-size: 13px; color: var(--sable); }
  .submit-note a { color: var(--bleu-moyen); text-decoration: none; font-weight: 600; }

  .success-msg {
    display: none;
    background: var(--bleu-fonce);
    color: white;
    padding: 24px 32px;
    border-radius: 4px;
    text-align: center;
    margin-top: 30px;
  }

  .success-msg h3 { font-family: 'Red Hat Display', sans-serif; font-size: 20px; font-weight: 700; margin-bottom: 8px; }
  .success-msg p { font-size: 14px; opacity: 0.85; }

  footer {
    background: var(--bleu-fonce);
    color: rgba(255,255,255,0.5);
    text-align: center;
    padding: 24px;
    font-size: 12px;
    letter-spacing: 0.05em;
    margin-top: 60px;
  }

  @media (max-width: 600px) {
    header { padding: 24px; flex-direction: column; gap: 16px; text-align: center; }
    .container { padding: 40px 20px; }
    .field-group { grid-template-columns: 1fr; }
    .interests-grid { grid-template-columns: 1fr; }
    .events-grid { grid-template-columns: 1fr; }
  }
</style>
</head>
<body>

<header>
  <div class="header-left">
    <h1>Club Korvell — Questionnaire de présentation</h1>
    <h2>Membre Structurant</h2>
  </div>
  <div class="badge">Experts & Partenaires</div>
</header>

<div class="container">

  <div class="intro">
    <p>Ce questionnaire nous permet de définir votre profil d'expertise, de vous positionner dans le réseau et de préparer votre présentation aux membres affiliés et aux gestionnaires partenaires. <strong>Votre contribution commence ici.</strong> Complétez toutes les sections et soumettez le formulaire.</p>
  </div>

  <form id="mainForm" onsubmit="handleSubmit(event)">

    <!-- SECTION 1 -->
    <div class="section">
      <div class="section-header">
        <div class="section-number">1</div>
        <div class="section-title">Informations sur l'entreprise</div>
      </div>

      <div class="field-group">
        <div class="field">
          <label>Nom de l'entreprise <span class="required">*</span></label>
          <input type="text" placeholder="Ex. : Stratégie & Gestion Conseil Inc." required>
        </div>
        <div class="field">
          <label>Nom du représentant principal <span class="required">*</span></label>
          <input type="text" placeholder="Prénom et nom" required>
        </div>
      </div>

      <div class="field-group">
        <div class="field">
          <label>Titre / Fonction <span class="required">*</span></label>
          <input type="text" placeholder="Ex. : Directeur général, Consultant principal" required>
        </div>
        <div class="field">
          <label>Téléphone professionnel <span class="required">*</span></label>
          <input type="tel" placeholder="Ex. : 514 000-0000" required>
        </div>
      </div>

      <div class="field-group">
        <div class="field">
          <label>Adresse courriel professionnelle <span class="required">*</span></label>
          <input type="email" placeholder="info@votreentreprise.com" required>
        </div>
        <div class="field">
          <label>Site web</label>
          <input type="url" placeholder="www.votreentreprise.com">
        </div>
      </div>

      <div class="field-group full">
        <div class="field">
          <label>Réseaux sociaux</label>
          <input type="text" placeholder="LinkedIn, Instagram, Facebook — indiquez les liens ou noms de page">
        </div>
      </div>
    </div>

    <!-- SECTION 2 -->
    <div class="section">
      <div class="section-header">
        <div class="section-number">2</div>
        <div class="section-title">Domaines d'expertise</div>
      </div>

      <p style="font-size:14px; margin-bottom:18px; line-height:1.6;">Sélectionnez vos domaines d'expertise principaux. Ces informations seront utilisées pour vous mettre en relation avec les membres affiliés qui ont besoin de votre soutien.</p>

      <div class="tags-container" id="expertiseTags">
        <div class="tag" onclick="toggleTag(this)">Gestion commerciale</div>
        <div class="tag" onclick="toggleTag(this)">Technologies & informatique</div>
        <div class="tag" onclick="toggleTag(this)">Ressources humaines</div>
        <div class="tag" onclick="toggleTag(this)">Finance & comptabilité</div>
        <div class="tag" onclick="toggleTag(this)">Marketing & communications</div>
        <div class="tag" onclick="toggleTag(this)">Formation professionnelle</div>
        <div class="tag" onclick="toggleTag(this)">Juridique & conformité</div>
        <div class="tag" onclick="toggleTag(this)">Gestion de projets</div>
        <div class="tag" onclick="toggleTag(this)">Stratégie d'entreprise</div>
        <div class="tag" onclick="toggleTag(this)">Optimisation des opérations</div>
        <div class="tag" onclick="toggleTag(this)">Développement des affaires</div>
        <div class="tag" onclick="toggleTag(this)">Autre</div>
      </div>

      <div class="field-group full" style="margin-top:16px;">
        <div class="field">
          <label>Précisez votre expertise (si nécessaire)</label>
          <input type="text" placeholder="Ex. : Implantation d'outils de gestion pour PME de services, coaching de dirigeants…">
        </div>
      </div>

      <div class="field-group">
        <div class="field">
          <label>Types d'intervention que vous offrez <span class="required">*</span></label>
          <select required>
            <option value="" disabled selected>Sélectionnez le type principal</option>
            <option>Audit & diagnostic</option>
            <option>Formation & ateliers</option>
            <option>Coaching & accompagnement</option>
            <option>Implantation d'outils ou systèmes</option>
            <option>Conseil stratégique</option>
            <option>Gestion de projet ponctuelle</option>
            <option>Plusieurs types selon le besoin</option>
          </select>
        </div>
        <div class="field">
          <label>Capacité d'accompagnement simultané <span class="required">*</span></label>
          <select required>
            <option value="" disabled selected>Sélectionnez</option>
            <option>1 à 3 membres simultanément</option>
            <option>4 à 7 membres simultanément</option>
            <option>8 membres et plus</option>
          </select>
        </div>
      </div>

      <div class="field-group full">
        <div class="field">
          <label>Zones géographiques couvertes <span class="required">*</span></label>
          <input type="text" placeholder="Ex. : Montréal, Laval, Rive-Sud — ou partout au Québec si services en ligne" required>
        </div>
      </div>

      <div class="field-group full">
        <div class="field">
          <label>Ce que les membres affiliés gagnent à travailler avec vous <span class="required">*</span></label>
          <textarea placeholder="Comment votre expertise leur permet-elle de croître, de mieux gérer leur volume ou d'améliorer leur exécution ?" required></textarea>
        </div>
      </div>
    </div>

    <!-- SECTION 3 -->
    <div class="section">
      <div class="section-header">
        <div class="section-number">3</div>
        <div class="section-title">Visuels pour votre fiche membre</div>
      </div>

      <div class="field-group">
        <div class="field">
          <label>Logo de l'entreprise <span class="required">*</span></label>
          <div class="upload-zone" onclick="document.getElementById('logoUpload').click()">
            <input type="file" id="logoUpload" accept=".png,.jpg,.jpeg,.svg" onchange="showPreview(this, 'logoPreview')">
            <span class="upload-icon">🏢</span>
            <p>Cliquez pour téléverser votre logo</p>
            <span>PNG, JPG, SVG — Résolution minimale recommandée : 300 dpi</span>
            <div class="upload-preview" id="logoPreview"></div>
          </div>
        </div>
        <div class="field">
          <label>Photo du représentant principal</label>
          <div class="upload-zone" onclick="document.getElementById('photoUpload').click()">
            <input type="file" id="photoUpload" accept=".png,.jpg,.jpeg" onchange="showPreview(this, 'photoPreview')">
            <span class="upload-icon">👤</span>
            <p>Cliquez pour téléverser votre photo</p>
            <span>PNG, JPG — Photo professionnelle recommandée</span>
            <div class="upload-preview" id="photoPreview"></div>
          </div>
        </div>
      </div>
    </div>

    <!-- SECTION 4 -->
    <div class="section">
      <div class="section-header">
        <div class="section-number">4</div>
        <div class="section-title">Intérêts dans le Club</div>
      </div>

      <p style="font-size:14px; margin-bottom: 20px; line-height:1.6;">Sélectionnez tout ce qui s'applique.</p>

      <div class="interests-grid">
        <label class="interest-item">
          <input type="checkbox" onchange="toggleChecked(this)">
          <span>Participer activement aux événements du Club</span>
        </label>
        <label class="interest-item">
          <input type="checkbox" onchange="toggleChecked(this)">
          <span>Devenir formateur ou conférencier au sein du Club</span>
        </label>
        <label class="interest-item">
          <input type="checkbox" onchange="toggleChecked(this)">
          <span>Offrir des ateliers pratiques aux membres affiliés</span>
        </label>
        <label class="interest-item">
          <input type="checkbox" onchange="toggleChecked(this)">
          <span>Participer au Comité des membres (rôle consultatif)</span>
        </label>
        <label class="interest-item">
          <input type="checkbox" onchange="toggleChecked(this)">
          <span>Commanditer un événement Korvell</span>
        </label>
        <label class="interest-item">
          <input type="checkbox" onchange="toggleChecked(this)">
          <span>Organiser un événement privé dans le cadre du Club</span>
        </label>
      </div>
    </div>

    <!-- SECTION 5 -->
    <div class="section">
      <div class="section-header">
        <div class="section-number">5</div>
        <div class="section-title">Confirmation de présence — Événements 2026</div>
      </div>

      <p style="font-size:14px; margin-bottom: 20px; line-height:1.6; font-weight:600; color: var(--bleu-fonce);">La participation aux trois événements est obligatoire pour tous les membres.</p>

      <div class="events-grid">
        <div class="event-card">
          <div class="event-month">JUIN 2026</div>
          <div class="event-label">Événement d'accueil #1</div>
          <div class="event-desc">Présentation des premières avancées du Club aux membres et gestionnaires partenaires.</div>
        </div>
        <div class="event-card">
          <div class="event-month">AOÛT 2026</div>
          <div class="event-label">Événement d'accueil #2</div>
          <div class="event-desc">Mise à jour des avancées du réseau et renforcement des liens.</div>
        </div>
        <div class="event-card lancement">
          <div class="event-month">SEPTEMBRE 2026</div>
          <div class="event-label">Lancement officiel</div>
          <div class="event-desc">Ouverture officielle de Korvell et du Club Korvell. Présence de tous les membres requise.</div>
        </div>
      </div>

      <div class="events-note">
        En soumettant ce formulaire, vous confirmez avoir pris connaissance des trois dates et vous engagez à y participer.
      </div>
    </div>

    <div class="submit-area">
      <button type="submit" class="submit-btn">Soumettre ma fiche membre →</button>
      <p class="submit-note">Une confirmation sera envoyée à votre adresse courriel. Questions ? <a href="mailto:veronique@clubkorvell.com">veronique@clubkorvell.com</a></p>
    </div>

    <div class="success-msg" id="successMsg">
      <h3>✓ Questionnaire reçu !</h3>
      <p>Merci. Véronique vous contactera sous peu pour finaliser votre intégration dans le réseau Club Korvell.</p>
    </div>
  </form>
</div>

<footer>
  Club Korvell &nbsp;·&nbsp; 1441 Boul. René-Lévesque O, Montréal, QC H3G 1T8 &nbsp;·&nbsp; veronique@clubkorvell.com &nbsp;·&nbsp; clubkorvell.com
</footer>

<script>
  function showPreview(input, previewId) {
    const preview = document.getElementById(previewId);
    if (input.files && input.files[0]) {
      preview.style.display = 'block';
      preview.textContent = '✓ ' + input.files[0].name;
    }
  }

  function toggleTag(el) {
    el.classList.toggle('selected');
  }

  function toggleChecked(checkbox) {
    checkbox.closest('.interest-item').classList.toggle('checked', checkbox.checked);
  }

  function handleSubmit(e) {
    e.preventDefault();
    const btn = document.querySelector('.submit-btn');
    btn.textContent = 'Envoi en cours...';
    btn.disabled = true;
    setTimeout(() => {
      document.getElementById('successMsg').style.display = 'block';
      document.getElementById('successMsg').scrollIntoView({ behavior: 'smooth' });
      btn.textContent = '✓ Soumis';
    }, 1200);
  }
</script>

</body>
</html>
