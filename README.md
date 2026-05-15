<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
  <title>UoL LLB Guide | Exam Success Companion</title>
  <!-- Tailwind CSS CDN -->
  <script src="https://cdn.tailwindcss.com"></script>
  <!-- Custom Tailwind configuration to avoid conflicts -->
  <script>
    tailwind.config = {
      theme: {
        extend: {
          animation: {
            fadeIn: 'fadeIn 0.3s ease-out',
          },
          keyframes: {
            fadeIn: {
              from: { opacity: '0', transform: 'translateY(-10px)' },
              to: { opacity: '1', transform: 'translateY(0)' },
            }
          }
        }
      }
    }
  </script>
  <!-- Font Awesome (optional but safe) and Lucide is not needed, we use emojis / simple icons via HTML -->
  <style>
    /* Smooth scrolling and any fallback */
    html {
      scroll-behavior: smooth;
    }
    body {
      overflow-x: hidden;
    }
    /* Custom focus ring */
    *:focus {
      outline: none;
      ring: 2px solid #3b82f6;
    }
  </style>
</head>
<body class="bg-gradient-to-br from-slate-50 via-blue-50 to-indigo-50 antialiased">

  <div class="min-h-screen">
    <!-- Header with sticky behavior -->
    <header class="bg-gradient-to-r from-slate-900 via-blue-900 to-indigo-900 text-white sticky top-0 z-50 shadow-2xl">
      <div class="container mx-auto px-4 py-6">
        <div class="flex items-center justify-between flex-wrap gap-4">
          <div>
            <h1 class="text-3xl md:text-4xl font-bold tracking-tight">UoL LLB Guide</h1>
            <p class="text-blue-200 text-sm mt-1">Your Complete Exam Success Companion</p>
          </div>
          <!-- Book icon via simple SVG (replaces Lucide) -->
          <svg xmlns="http://www.w3.org/2000/svg" class="w-12 h-12 text-blue-300" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
            <path stroke-linecap="round" stroke-linejoin="round" d="M12 6.253v13m0-13C10.832 5.477 9.246 5 7.5 5S4.168 5.477 3 6.253v13C4.168 18.477 5.754 18 7.5 18s3.332.477 4.5 1.253m0-13C13.168 5.477 14.754 5 16.5 5c1.747 0 3.332.477 4.5 1.253v13C19.832 18.477 18.247 18 16.5 18c-1.746 0-3.332.477-4.5 1.253" />
          </svg>
        </div>
        
        <nav class="mt-6 flex flex-wrap gap-2">
          <button data-section="home" class="nav-btn px-4 py-2 rounded-lg transition-all duration-300 bg-white text-blue-900 shadow-lg transform scale-105">Home</button>
          <button data-section="modules" class="nav-btn px-4 py-2 rounded-lg transition-all duration-300 bg-blue-800/50 hover:bg-blue-700 text-white">Modules</button>
          <button data-section="exam-guidance" class="nav-btn px-4 py-2 rounded-lg transition-all duration-300 bg-blue-800/50 hover:bg-blue-700 text-white">Exam Guidance</button>
          <button data-section="purchase" class="nav-btn px-4 py-2 rounded-lg transition-all duration-300 bg-blue-800/50 hover:bg-blue-700 text-white">Purchase</button>
          <button data-section="about" class="nav-btn px-4 py-2 rounded-lg transition-all duration-300 bg-blue-800/50 hover:bg-blue-700 text-white">About</button>
          <button data-section="complaints" class="nav-btn px-4 py-2 rounded-lg transition-all duration-300 bg-blue-800/50 hover:bg-blue-700 text-white">Complaints</button>
        </nav>
      </div>
    </header>

    <main class="container mx-auto px-4 py-12">
      <!-- HOME Section -->
      <section id="home" class="mb-20 scroll-mt-24">
        <div class="bg-white rounded-3xl shadow-2xl p-8 md:p-12 border-t-4 border-blue-600">
          <h2 class="text-5xl font-bold text-slate-900 mb-6">Welcome to Your LLB Success Journey</h2>
          <p class="text-xl text-slate-700 leading-relaxed mb-6">
            This comprehensive guide is designed to help University of London LLB students navigate their academic journey with confidence. 
            Access detailed information about exam structures, important topics, answer techniques, and study resources for all three levels.
          </p>
          <div class="grid md:grid-cols-3 gap-6 mt-8">
            <div class="bg-gradient-to-br from-blue-50 to-indigo-50 p-6 rounded-xl border-2 border-blue-200">
              <svg xmlns="http://www.w3.org/2000/svg" class="w-10 h-10 text-blue-600 mb-3" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.8" d="M9 12h6m-6 4h6m2 5H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z" /></svg>
              <h3 class="text-xl font-bold text-slate-900 mb-2">Complete Module Coverage</h3>
              <p class="text-slate-700">All Level 4, 5, and 6 modules with exam patterns and important topics</p>
            </div>
            <div class="bg-gradient-to-br from-indigo-50 to-purple-50 p-6 rounded-xl border-2 border-indigo-200">
              <svg xmlns="http://www.w3.org/2000/svg" class="w-10 h-10 text-indigo-600 mb-3" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.8" d="M12 6.253v13m0-13C10.832 5.477 9.246 5 7.5 5S4.168 5.477 3 6.253v13C4.168 18.477 5.754 18 7.5 18s3.332.477 4.5 1.253m0-13C13.168 5.477 14.754 5 16.5 5c1.747 0 3.332.477 4.5 1.253v13C19.832 18.477 18.247 18 16.5 18c-1.746 0-3.332.477-4.5 1.253" /></svg>
              <h3 class="text-xl font-bold text-slate-900 mb-2">Expert Exam Guidance</h3>
              <p class="text-slate-700">IRAC, ILAC, and advanced techniques for problem and essay questions</p>
            </div>
            <div class="bg-gradient-to-br from-purple-50 to-pink-50 p-6 rounded-xl border-2 border-purple-200">
              <svg xmlns="http://www.w3.org/2000/svg" class="w-10 h-10 text-purple-600 mb-3" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.8" d="M3 3h2l.4 2M7 13h10l4-8H5.4M7 13L5.4 5M7 13l-1.5 6M17 13l1.5 6M9 21h6M12 15v6" /></svg>
              <h3 class="text-xl font-bold text-slate-900 mb-2">Premium Study Notes</h3>
              <p class="text-slate-700">Affordable notes and custom question answers available for purchase</p>
            </div>
          </div>
        </div>
      </section>

      <!-- Qualifying Degree Section -->
      <section class="mb-20">
        <div class="bg-gradient-to-r from-amber-50 to-orange-50 rounded-3xl shadow-xl p-8 md:p-12 border-l-8 border-amber-500">
          <div class="flex items-start gap-4">
            <svg xmlns="http://www.w3.org/2000/svg" class="w-10 h-10 text-amber-600 flex-shrink-0 mt-1" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 9v2m0 4h.01m-6.938 4h13.856c1.54 0 2.502-1.667 1.732-3L13.732 4c-.77-1.333-2.694-1.333-3.464 0L3.34 16c-.77 1.333.192 3 1.732 3z" /></svg>
            <div>
              <h2 class="text-3xl font-bold text-slate-900 mb-4">Understanding Qualifying Degrees</h2>
              <p class="text-lg text-slate-800 leading-relaxed">
                For a University of London LLB, the key thing to understand is that while subjects like <span class="font-semibold">Tort Law, Property Law, and European Union Law</span> form part of the traditional core of a Qualifying Law Degree, your choice of optional modules does not determine whether you can become a lawyer. Entry into the Solicitors Qualifying Examination or the Bar is based on passing professional training stages, not specific module selection.
              </p>
              <p class="text-lg text-slate-800 leading-relaxed mt-4">
                However, choosing academically strong and relevant modules can give you a real advantage in legal understanding, exam performance, and future preparation, even though it is not a strict requirement.
              </p>
            </div>
          </div>
        </div>
      </section>

      <!-- MODULES Section (dynamic via JS but we can hardcode with interactivity) -->
      <section id="modules" class="mb-20 scroll-mt-24">
        <h2 class="text-5xl font-bold text-slate-900 mb-8 text-center">Module Directory</h2>
        <div id="modules-container" class="space-y-8"></div>
      </section>

      <!-- EXAM GUIDANCE Section -->
      <section id="exam-guidance" class="mb-20 scroll-mt-24">
        <h2 class="text-5xl font-bold text-slate-900 mb-8 text-center">Exam Guidance & Techniques</h2>
        <div class="grid lg:grid-cols-2 gap-8">
          <!-- Problem Questions -->
          <div class="bg-white rounded-3xl shadow-2xl p-8 border-t-4 border-green-500">
            <h3 class="text-3xl font-bold text-slate-900 mb-6">⚖️ Problem Questions</h3>
            <div class="space-y-6">
              <div><h4 class="text-2xl font-bold text-green-700 mb-3">IRAC Method</h4>
                <div class="space-y-4"><div class="bg-green-50 p-4 rounded-xl"><h5 class="font-bold">I - Issue</h5><p>Identify the legal question precisely</p><p class="text-sm text-green-700">✅ "Whether the wording satisfies certainty of intention for a valid express trust"</p></div>
                <div class="bg-green-50 p-4 rounded-xl"><h5 class="font-bold">R - Rule</h5><p>State the relevant legal principle with leading case authority.</p></div>
                <div class="bg-green-50 p-4 rounded-xl border-2 border-green-500"><h5 class="font-bold">A - Application (MOST IMPORTANT)</h5><p>Apply the rule directly to the facts. This is where marks are won.</p></div>
                <div class="bg-green-50 p-4 rounded-xl"><h5 class="font-bold">C - Conclusion</h5><p>Give a clear, reasoned answer.</p></div></div>
              </div>
              <div class="bg-blue-50 p-6 rounded-xl"><h4 class="font-bold text-xl">🔥 Advanced Tips</h4><ul class="list-disc pl-5"><li>ILAC: Issue - Law - Application - Conclusion</li><li>MIRAT: Material Facts - Issue - Rule - Application - Tentative Conclusion</li><li>"Apply, Don't Recite" - Link every principle to facts</li></ul></div>
            </div>
          </div>
          <!-- Essay Questions -->
          <div class="bg-white rounded-3xl shadow-2xl p-8 border-t-4 border-purple-500">
            <h3 class="text-3xl font-bold text-slate-900 mb-6">📝 Essay Questions</h3>
            <div class="space-y-4">
              <div class="bg-purple-50 p-5 rounded-xl"><h4 class="font-bold">"Discuss"</h4><p>Present multiple perspectives, engage in analysis, reach reasoned conclusion.</p></div>
              <div class="bg-purple-50 p-5 rounded-xl"><h4 class="font-bold">"To What Extent"</h4><p>Explicitly evaluative - argument FOR → AGAINST → final judgment.</p></div>
              <div class="bg-purple-50 p-5 rounded-xl"><h4 class="font-bold">"Critically Analyse"</h4><p>Assess effectiveness, fairness, policy implications, include case law + academic opinion.</p></div>
              <div class="bg-purple-50 p-5 rounded-xl"><h4 class="font-bold">"Assess / Evaluate"</h4><p>Measure strengths and weaknesses, judge value.</p></div>
            </div>
          </div>
        </div>
      </section>

      <!-- PURCHASE Section (static but functional forms) -->
      <section id="purchase" class="mb-20 scroll-mt-24">
        <div class="bg-gradient-to-br from-green-50 to-emerald-50 rounded-3xl shadow-2xl p-8 md:p-12 border-t-4 border-green-600">
          <div class="flex items-center gap-4 mb-8"><svg xmlns="http://www.w3.org/2000/svg" class="w-12 h-12 text-green-600" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.8" d="M3 3h2l.4 2M7 13h10l4-8H5.4M7 13L5.4 5M7 13l-1.5 6M17 13l1.5 6M9 21h6M12 15v6" /></svg><h2 class="text-5xl font-bold text-slate-900">Purchase Study Materials</h2></div>
          <div class="bg-gradient-to-r from-blue-600 to-indigo-600 text-white p-6 rounded-2xl mb-8 text-center"><p class="text-2xl font-bold">✅ Get structured, exam-ready answers for UoL papers</p></div>
          
          <!-- Simple summary -->
          <div class="text-slate-700 bg-white p-6 rounded-xl mb-8">
            <p class="font-bold text-lg">📌 Notes & Answer Tiers available: Basic, Standard (Best Seller), Premium. Contact via email for custom orders and bundle discounts (4/6/10 answers packs).</p>
            <p class="mt-2">📧 Orders & inquiries: <a href="mailto:umairahmad7643@gmail.com" class="text-blue-600 underline">umairahmad7643@gmail.com</a></p>
            <p class="mt-1">💰 Level 4 notes start at 1500 PKR per module. Answer tiers: Basic 500-1000 PKR, Standard 1000-2000 PKR, Premium 1500-3500 PKR.</p>
          </div>

          <!-- Order forms (Formspree) -->
          <div class="grid md:grid-cols-2 gap-8">
            <form action="https://formspree.io/f/mqenoeov" method="POST" class="bg-white p-6 rounded-2xl shadow-xl">
              <h3 class="text-2xl font-bold mb-4">📝 Order Notes</h3>
              <input type="text" name="name" placeholder="Your Name" required class="w-full mb-3 p-3 border rounded-xl"><input type="email" name="email" placeholder="Email" required class="w-full mb-3 p-3 border rounded-xl"><input type="text" name="module" placeholder="Module Name" required class="w-full mb-3 p-3 border rounded-xl"><textarea name="additional_info" rows="2" placeholder="Level & details" class="w-full mb-3 p-3 border rounded-xl"></textarea><button type="submit" class="w-full bg-green-600 text-white py-3 rounded-xl font-bold">Submit Notes Order</button>
            </form>
            <form action="https://formspree.io/f/xgodbanw" method="POST" class="bg-white p-6 rounded-2xl shadow-xl">
              <h3 class="text-2xl font-bold mb-4">❓ Submit Questions for Answers</h3>
              <input type="text" name="name" placeholder="Your Name" required class="w-full mb-3 p-3 border rounded-xl"><input type="email" name="email" placeholder="Email" required class="w-full mb-3 p-3 border rounded-xl"><select name="level" class="w-full mb-3 p-3 border rounded-xl"><option>Level 4</option><option>Level 5</option><option>Level 6</option></select><textarea name="questions" rows="4" placeholder="Paste your question(s)" required class="w-full mb-3 p-3 border rounded-xl"></textarea><button type="submit" class="w-full bg-blue-600 text-white py-3 rounded-xl font-bold">Submit for Answers</button>
            </form>
          </div>
        </div>
      </section>

      <!-- ABOUT Section -->
      <section id="about" class="mb-20 scroll-mt-24">
        <div class="bg-gradient-to-br from-blue-50 to-indigo-50 rounded-3xl shadow-2xl p-8 md:p-12 border-t-4 border-blue-600">
          <div class="flex items-center gap-4 mb-6"><svg xmlns="http://www.w3.org/2000/svg" class="w-12 h-12 text-blue-600" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.8" d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z" /></svg><h2 class="text-5xl font-bold text-slate-900">About the Founder</h2></div>
          <div class="bg-white p-8 rounded-2xl shadow-lg"><p class="text-lg text-slate-700">Created by a University of London LLB graduate who understands the challenges. Committed to providing comprehensive guidance. For Francis Ng articles (Tort Law & Equity and Trusts), contact via email.</p>
          <div class="mt-6 p-4 bg-green-50 rounded-xl"><h3 class="font-bold">📞 Contact: <a href="mailto:umairahmad7643@gmail.com" class="text-green-700 underline">umairahmad7643@gmail.com</a></h3></div></div>
        </div>
      </section>

      <!-- COMPLAINTS Section -->
      <section id="complaints" class="mb-20 scroll-mt-24">
        <div class="bg-gradient-to-br from-red-50 to-orange-50 rounded-3xl shadow-2xl p-8 md:p-12 border-t-4 border-red-600">
          <div class="flex items-center gap-4 mb-6"><svg xmlns="http://www.w3.org/2000/svg" class="w-12 h-12 text-red-600" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.8" d="M8 10h.01M12 10h.01M16 10h.01M9 16H5a2 2 0 01-2-2V6a2 2 0 012-2h14a2 2 0 012 2v8a2 2 0 01-2 2h-5l-5 5v-5z" /></svg><h2 class="text-5xl font-bold text-slate-900">Submit a Complaint</h2></div>
          <form action="https://formspree.io/f/mwvyjvdn" method="POST" class="bg-white p-8 rounded-2xl shadow-xl"><input type="text" name="name" placeholder="Your Name" required class="w-full mb-4 p-3 border rounded-xl"><input type="email" name="email" placeholder="Email" required class="w-full mb-4 p-3 border rounded-xl"><input type="text" name="module" placeholder="Module/Section" required class="w-full mb-4 p-3 border rounded-xl"><textarea name="complaint" rows="5" placeholder="Describe error" required class="w-full mb-4 p-3 border rounded-xl"></textarea><button type="submit" class="w-full bg-red-600 text-white py-3 rounded-xl font-bold">Submit Complaint</button></form>
        </div>
      </section>
    </main>

    <footer class="bg-gradient-to-r from-slate-900 via-blue-900 to-indigo-900 text-white py-12">
      <div class="container mx-auto px-4 text-center"><h3 class="text-2xl font-bold mb-2">UoL LLB Guide</h3><p class="text-blue-200">Empowering University of London LLB Students</p><p class="text-sm mt-4">© 2025 UoL LLB Guide. All rights reserved.</p><div class="mt-4"><a href="mailto:umairahmad7643@gmail.com" class="inline-flex gap-2 text-blue-200 hover:text-white">📧 umairahmad7643@gmail.com</a></div></div>
    </footer>
  </div>

  <!-- JavaScript for dynamic modules and active section highlighting -->
  <script>
    // Module data
    const levelsData = {
      level4: { title: 'Level 4 (Year 1)', price: '1500 PKR per module', modules: [{ code: 'LA 1040', name: 'Contract Law', pattern: 'Attempt four questions from a choice of eight questions.', topics: ['Offer and Acceptance','Intention','Consideration','Misrepresentation','Mistake','Frustration','Breach of Contract'] },{ code: 'LA 1010', name: 'Criminal Law', pattern: 'Part A: Compulsory Question | Part B: Attempt three questions.', topics: ['Actus Reus & Mens Rea','Rape','Offences Against Persons','Property Offences','Criminal Damage','Criminal Attempt','Participation in Crime'] },{ code: 'LA 1020', name: 'Public Law', pattern: 'Part A: Compulsory | Part B: Attempt three from seven.', topics: ['Rule of Law','Parliamentary Sovereignty','Royal Prerogative','Human Rights Act','Judicial Review'] },{ code: 'LA 1031', name: 'Legal System and Method', pattern: 'Part A: MCQs | Part B: Attempt two questions', topics: ['Judicial Precedent','Statutory Interpretation'] }] },
      level5: { title: 'Level 5 (Year 2)', price: '2000 PKR per module', modules: [{ code: 'LA 2001', name: 'Tort Law', pattern: 'Part A: Compulsory | Part B: Attempt three from eight', topics: ['Negligence','Psychiatric Harm','Pure Economic Loss','Occupiers Liability','Vicarious Liability','Nuisance'] },{ code: 'LA 2003', name: 'Property Law', pattern: 'Part A & B mix', topics: ['Unregistered/Registered Land','Adverse Possession','Easements','Mortgage','Co-ownership'] },{ code: 'LA 2024', name: 'EU Law', required: true, pattern: 'Answer four from eight', topics: ['Direct Effect','Free Movement','Preliminary Referencing'] },{ code: 'LA 2029', name: 'International Protection of Human Rights', optional: true, pattern: 'Attempt three from seven', topics: ['Universalism vs Culturalism','Women Rights','Refugee Rights'] }] },
      level6: { title: 'Level 6 (Final Year)', price: '2500 PKR per module', modules: [{ code: 'LA 1011', name: 'Jurisprudence', required: true, pattern: 'Part A Compulsory | Part B three from nine', topics: ['Naturalism','Liberalism','Command Theory','Marxism','Feminism'] },{ code: 'LA 3015', name: 'Equity and Trusts', optional: true, pattern: 'Part A Compulsory article | Part B three from eight', topics: ['Three Certainties','Charitable Trusts','Resulting Trust','Constructive Trust'] },{ code: 'LA 3012', name: 'Company Law', optional: true, pattern: 'Essay & Problem', topics: ['Separate Legal Personality','Director Duties','Minority Protection'] },{ code: 'LA 3011', name: 'Alternative Dispute Resolution', optional: true, pattern: 'Compulsory + problems', topics: ['Mediation','Arbitration','ADR vs Litigation'] }] }
    };

    let expandedLevel = null;
    let expandedModuleKey = null;

    function renderModules() {
      const container = document.getElementById('modules-container');
      if (!container) return;
      container.innerHTML = '';
      for (const [levelKey, level] of Object.entries(levelsData)) {
        const levelDiv = document.createElement('div');
        levelDiv.className = 'mb-8';
        const btn = document.createElement('button');
        btn.className = 'w-full bg-gradient-to-r from-blue-600 to-indigo-600 text-white p-6 rounded-2xl shadow-xl hover:shadow-2xl transition-all duration-300 flex items-center justify-between group';
        btn.innerHTML = `<div class="text-left"><h3 class="text-3xl font-bold">${level.title}</h3><p class="text-blue-100 mt-1">${level.price}</p></div><svg xmlns="http://www.w3.org/2000/svg" class="w-8 h-8 transition-transform duration-300 ${expandedLevel === levelKey ? 'rotate-180' : ''}" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" /></svg>`;
        btn.addEventListener('click', () => {
          expandedLevel = expandedLevel === levelKey ? null : levelKey;
          renderModules();
        });
        levelDiv.appendChild(btn);
        if (expandedLevel === levelKey) {
          const modulesContainer = document.createElement('div');
          modulesContainer.className = 'mt-4 space-y-4 animate-fadeIn';
          level.modules.forEach((mod, idx) => {
            const modCard = document.createElement('div');
            modCard.className = 'bg-white rounded-2xl shadow-lg overflow-hidden border-l-4 border-blue-500';
            const modBtn = document.createElement('button');
            modBtn.className = 'w-full p-6 text-left hover:bg-slate-50 transition-colors flex items-center justify-between';
            const isExpanded = expandedModuleKey === `${levelKey}-${idx}`;
            modBtn.innerHTML = `<div class="flex-1"><div class="flex gap-2 mb-2"><span class="px-3 py-1 bg-blue-100 text-blue-800 rounded-full text-sm font-semibold">${mod.code}</span>${mod.required ? '<span class="px-3 py-1 bg-green-100 text-green-800 rounded-full text-sm font-semibold">Required</span>' : ''}${mod.optional ? '<span class="px-3 py-1 bg-amber-100 text-amber-800 rounded-full text-sm font-semibold">Optional</span>' : ''}</div><h4 class="text-2xl font-bold text-slate-900">${mod.name}</h4></div><svg xmlns="http://www.w3.org/2000/svg" class="w-6 h-6 text-slate-600 transition-transform ${isExpanded ? 'rotate-180' : ''}" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" /></svg>`;
            modBtn.addEventListener('click', (e) => {
              e.stopPropagation();
              expandedModuleKey = expandedModuleKey === `${levelKey}-${idx}` ? null : `${levelKey}-${idx}`;
              renderModules();
            });
            modCard.appendChild(modBtn);
            if (isExpanded) {
              const detailsDiv = document.createElement('div');
              detailsDiv.className = 'p-6 bg-slate-50 border-t border-slate-200';
              detailsDiv.innerHTML = `<div class="mb-4"><h5 class="text-lg font-bold mb-2">📋 Exam Pattern:</h5><p class="text-slate-700">${mod.pattern}</p></div><div><h5 class="text-lg font-bold mb-3">🎯 Important Topics:</h5><ul class="space-y-2">${mod.topics.map(t => `<li class="flex gap-2"><span class="text-blue-600">▸</span><span class="text-slate-700">${t}</span></li>`).join('')}</ul></div>`;
              modCard.appendChild(detailsDiv);
            }
            modulesContainer.appendChild(modCard);
          });
          levelDiv.appendChild(modulesContainer);
        }
        container.appendChild(levelDiv);
      }
    }

    // Active section highlight & smooth scroll
    const sections = ['home', 'modules', 'exam-guidance', 'purchase', 'about', 'complaints'];
    const navBtns = document.querySelectorAll('.nav-btn');
    function updateActiveSection() {
      const scrollPos = window.scrollY + 150;
      let current = 'home';
      for (const sec of sections) {
        const el = document.getElementById(sec);
        if (el && el.offsetTop <= scrollPos) current = sec;
      }
      navBtns.forEach(btn => {
        const section = btn.getAttribute('data-section');
        if (section === current) {
          btn.classList.remove('bg-blue-800/50', 'hover:bg-blue-700');
          btn.classList.add('bg-white', 'text-blue-900', 'shadow-lg', 'transform', 'scale-105');
        } else {
          btn.classList.remove('bg-white', 'text-blue-900', 'shadow-lg', 'transform', 'scale-105');
          btn.classList.add('bg-blue-800/50', 'hover:bg-blue-700', 'text-white');
        }
      });
    }
    navBtns.forEach(btn => {
      btn.addEventListener('click', () => {
        const sectionId = btn.getAttribute('data-section');
        const target = document.getElementById(sectionId);
        if (target) target.scrollIntoView({ behavior: 'smooth' });
      });
    });
    window.addEventListener('scroll', updateActiveSection);
    window.addEventListener('load', () => {
      renderModules();
      updateActiveSection();
    });
  </script>
</body>
</html>
