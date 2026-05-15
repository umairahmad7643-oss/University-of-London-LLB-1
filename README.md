import React, { useState } from 'react';
import { ChevronDown, Mail, BookOpen, FileText, AlertCircle, User, ShoppingCart, MessageSquare } from 'lucide-react';

export default function UoLLBGuide() {
  const [activeSection, setActiveSection] = useState('home');
  const [expandedLevel, setExpandedLevel] = useState(null);
  const [expandedModule, setExpandedModule] = useState(null);

  const scrollToSection = (sectionId) => {
    setActiveSection(sectionId);
    const element = document.getElementById(sectionId);
    if (element) {
      element.scrollIntoView({ behavior: 'smooth' });
    }
  };

  const levels = {
    level4: {
      title: 'Level 4 (Year 1)',
      price: '1500 PKR per module',
      modules: [
        {
          code: 'LA 1040',
          name: 'Contract Law',
          pattern: 'Attempt four questions from a choice of eight questions.',
          topics: [
            'Offer and Acceptance',
            'Intention',
            'Consideration',
            'Misrepresentation',
            'Mistake',
            'Frustration',
            'Breach of Contract'
          ]
        },
        {
          code: 'LA 1010',
          name: 'Criminal Law',
          pattern: 'Part A: Compulsory Question | Part B: Attempt three questions from a choice of six questions.',
          topics: [
            'Actus Reus & Mens Rea (Basics)',
            'Rape',
            'Offences Against Persons',
            'Property Offences',
            'Criminal Damage',
            'Criminal Attempt',
            'Participation in Crime'
          ]
        },
        {
          code: 'LA 1020',
          name: 'Public Law',
          pattern: 'Part A: Compulsory Question | Part B: Attempt three questions from a choice of seven questions.',
          topics: [
            'Rule of Law',
            'Parliamentary Sovereignty',
            'Royal Prerogative',
            'Codified and Uncodified Constitution',
            'Human Rights Act',
            'Judicial Review'
          ]
        },
        {
          code: 'LA 1031',
          name: 'Legal System and Method',
          pattern: 'Part A: MCQs | Part B: Attempt two questions from a choice of six questions | Part C: Compulsory Question',
          topics: [
            'Judicial Precedent and Judicial Law Making',
            'Statutory Interpretation'
          ]
        }
      ]
    },
    level5: {
      title: 'Level 5 (Year 2)',
      price: '2000 PKR per module',
      modules: [
        {
          code: 'LA 2001',
          name: 'Tort Law',
          pattern: 'Part A: Compulsory Question (Article by Francis Ng) | Part B: Attempt three questions from a choice of eight questions.',
          note: 'For the article contact the number under about the founder section.',
          topics: [
            'Negligence (Duty of Care, Breach, Causation, Remoteness, Damages, Defences)',
            'Psychiatric Harm',
            'Pure Economic Loss (PEL)',
            'Occupiers Liability Act (OLA)',
            'Vicarious Liability',
            'Nuisance (Public/Private) & Rylands v Fletcher'
          ]
        },
        {
          code: 'LA 2003',
          name: 'Property Law',
          pattern: 'Part A: Compulsory Question | Part B: Attempt at least one question | Part C: Attempt at least one question. You can choose to answer the last question from either Part A or Part B.',
          topics: [
            'Unregistered and Registered Land',
            'Adverse Possession',
            'Easements',
            'Mortgage',
            'Licenses and Leases',
            'Co-ownership',
            'Proprietary Estoppel'
          ]
        },
        {
          code: 'LA 2024',
          name: 'EU Law',
          required: true,
          pattern: 'Answer four questions from a choice of eight questions.',
          topics: [
            'Essay: Direct Effect, Citizenship, Charter of Fundamental Rights, Preliminary Referencing',
            'Problem: Direct Effect, Free movement of goods, Free movement of citizens and workers, Competition Policy, State Liability'
          ]
        },
        {
          code: 'LA 2029',
          name: 'International Protection of Human Rights',
          optional: true,
          pattern: 'Attempt three questions from a choice of seven questions.',
          topics: [
            'Universalism vs Culturalism',
            'Women\'s Rights (CEDAW)',
            'Refugee Rights',
            'Child Rights',
            'Religious Discrimination',
            'Genocide and Crimes Against Humanity'
          ]
        },
        {
          code: 'LA 2019',
          name: 'Family Law',
          optional: true,
          pattern: 'Attempt four questions from a choice of eight questions.',
          topics: [
            'Relationship Status',
            'Dissolution',
            'Financial Matters',
            'Domestic Abuse',
            'Children and Parentage',
            'State Intervention',
            'Adoption'
          ]
        },
        {
          code: 'LA 2017',
          name: 'Commercial Law',
          optional: true,
          pattern: 'Attempt three questions from a choice of six questions.',
          topics: [
            'Sales of Goods Act 1979',
            'International Sales',
            'Consumer Protection',
            'Agency and Security'
          ]
        },
        {
          code: 'LA 2008',
          name: 'Administrative Law',
          optional: true,
          pattern: 'Attempt three questions from a choice of six questions.',
          topics: [
            'Foundation: Theory of Administrative law',
            'Government Processes',
            'Judicial Review',
            'Alternative Controls',
            'Liability Rights'
          ]
        },
        {
          code: 'LA 2010',
          name: 'Introduction to Criminology',
          optional: true,
          pattern: 'Contact for details',
          topics: []
        }
      ]
    },
    level6: {
      title: 'Level 6 (Final Year)',
      price: '2500 PKR per module',
      modules: [
        {
          code: 'LA 1011',
          name: 'Jurisprudence',
          required: true,
          pattern: 'Part A: Compulsory | Part B: Attempt three questions from a choice of nine questions.',
          topics: [
            'Part A: Naturalism, Liberalism, Ronald Dworkin\'s Theory',
            'Part B: Command Theory (John Austin), Marxism (Karl Marx), Pure Theory (Kelsen), Feminism, Distributive Theory (John Rawls)'
          ]
        },
        {
          code: 'LA 3015',
          name: 'Equity and Trusts',
          optional: true,
          pattern: 'Part A: Compulsory (25 marks - Legal Article by Francis Ng) | Part B: Attempt three questions from a choice of eight questions.',
          topics: [
            'Three Certainties',
            'Formalities',
            'Constitution',
            'Charitable Purpose Trusts',
            'Private Purpose Trust',
            'Resulting Trust',
            'Constructive Trust (backup)'
          ]
        },
        {
          code: 'LA 3012',
          name: 'Company Law',
          optional: true,
          pattern: 'Part A: Essay - Attempt one question from a choice of 4 | Part B: Problem - Attempt one question from a choice of 4. Choose more from either part.',
          topics: [
            'Forms of Business Organization',
            'Separate Legal Personality',
            'Lifting Veil of Incorporation',
            'Management of the Company',
            'Director Duties',
            'Enforcing Director Duties',
            'Statutory Minority Protection'
          ]
        },
        {
          code: 'LA 3011',
          name: 'Alternative Dispute Resolution',
          optional: true,
          pattern: 'Part A: Compulsory | Part B: Attempt two problem questions from a choice of three | Part C: Attempt one essay question from a choice of two.',
          topics: [
            'Nature & Purpose of ADR',
            'Negotiation',
            'Mediation (VERY IMPORTANT)',
            'Arbitration (MOST IMPORTANT)',
            'Arbitration Law & Principles',
            'Confidentiality & Without Prejudice Rule',
            'ADR vs Litigation',
            'Ethics in ADR'
          ]
        },
        {
          code: 'LA 3013',
          name: 'Conflict of Laws',
          optional: true,
          pattern: 'Attempt three questions from a choice of six questions.',
          topics: [
            'Domicile',
            'Jurisdiction',
            'Choice of Law-Tort',
            'Choice of Law Contract'
          ]
        },
        {
          code: 'LA 3014',
          name: 'Criminology',
          optional: true,
          pattern: 'Attempt four questions from a choice of eight questions.',
          topics: [
            'Crime Theories (CORE)',
            'Causes of Crime',
            'Punishment & Sentencing',
            'Policing & Social Control',
            'Victimology'
          ]
        },
        {
          code: 'LA 3016',
          name: 'Evidence',
          optional: true,
          pattern: 'Answer four questions from a choice of eight questions.',
          topics: [
            'Burden & Standard of Proof (CORE)',
            'Admissibility of Evidence',
            'Hearsay Evidence (VERY IMPORTANT)',
            'Confessions',
            'Character Evidence',
            'Witnesses',
            'Illegally Obtained Evidence'
          ]
        },
        {
          code: 'LA 3017',
          name: 'Intellectual Property',
          optional: true,
          pattern: 'Answer three questions from a choice of six questions.',
          topics: [
            'Copyright (VERY IMPORTANT)',
            'Patents',
            'Trademarks',
            'Defences & Exceptions',
            'IP vs Public Access'
          ]
        },
        {
          code: 'LA 3018',
          name: 'Public International Law',
          optional: true,
          pattern: 'Attempt four questions from a choice of eight questions.',
          topics: [
            'Sources of International Law (CORE)',
            'State Responsibility (VERY IMPORTANT)',
            'Use of Force',
            'Jurisdiction',
            'International Courts (ICJ)',
            'Sovereignty vs Intervention'
          ]
        },
        {
          code: 'LA 3019',
          name: 'Introduction to Islamic Law',
          optional: true,
          pattern: 'Part A: Essay - Attempt at least one | Part B: Problem - Attempt at least one. Choose the last question from either part.',
          topics: [
            'Essay: Primary Sources (Quran & Sunnah), Secondary Sources (Qiyas & Ijma), Istihsan, Istishab, Ijtihad, Usul-Al-Fiqh, Six Periods of Islamic History',
            'Problem: Family Law (Marriage, Polygamy, Dissolution, Custody, Dowry, Maintenance), Penal Law (Hudud, Tazir, Qisas & Diyat), Financial Law (backup)'
          ]
        }
      ]
    }
  };

  return (
    <div className="min-h-screen bg-gradient-to-br from-slate-50 via-blue-50 to-indigo-50">
      {/* Header */}
      <header className="bg-gradient-to-r from-slate-900 via-blue-900 to-indigo-900 text-white sticky top-0 z-50 shadow-2xl">
        <div className="container mx-auto px-4 py-6">
          <div className="flex items-center justify-between">
            <div>
              <h1 className="text-3xl md:text-4xl font-bold tracking-tight">UoL LLB Guide</h1>
              <p className="text-blue-200 text-sm mt-1">Your Complete Exam Success Companion</p>
            </div>
            <BookOpen className="w-12 h-12 text-blue-300" />
          </div>
          
          <nav className="mt-6 flex flex-wrap gap-2">
            {['home', 'modules', 'exam-guidance', 'purchase', 'about', 'complaints'].map((section) => (
              <button
                key={section}
                onClick={() => scrollToSection(section)}
                className={`px-4 py-2 rounded-lg transition-all duration-300 ${
                  activeSection === section
                    ? 'bg-white text-blue-900 shadow-lg transform scale-105'
                    : 'bg-blue-800/50 hover:bg-blue-700 text-white'
                }`}
              >
                {section.split('-').map(word => word.charAt(0).toUpperCase() + word.slice(1)).join(' ')}
              </button>
            ))}
          </nav>
        </div>
      </header>

      <main className="container mx-auto px-4 py-12">
        {/* Home Section */}
        <section id="home" className="mb-20">
          <div className="bg-white rounded-3xl shadow-2xl p-8 md:p-12 border-t-4 border-blue-600">
            <h2 className="text-5xl font-bold text-slate-900 mb-6">Welcome to Your LLB Success Journey</h2>
            <p className="text-xl text-slate-700 leading-relaxed mb-6">
              This comprehensive guide is designed to help University of London LLB students navigate their academic journey with confidence. 
              Access detailed information about exam structures, important topics, answer techniques, and study resources for all three levels.
            </p>
            <div className="grid md:grid-cols-3 gap-6 mt-8">
              <div className="bg-gradient-to-br from-blue-50 to-indigo-50 p-6 rounded-xl border-2 border-blue-200">
                <FileText className="w-10 h-10 text-blue-600 mb-3" />
                <h3 className="text-xl font-bold text-slate-900 mb-2">Complete Module Coverage</h3>
                <p className="text-slate-700">All Level 4, 5, and 6 modules with exam patterns and important topics</p>
              </div>
              <div className="bg-gradient-to-br from-indigo-50 to-purple-50 p-6 rounded-xl border-2 border-indigo-200">
                <BookOpen className="w-10 h-10 text-indigo-600 mb-3" />
                <h3 className="text-xl font-bold text-slate-900 mb-2">Expert Exam Guidance</h3>
                <p className="text-slate-700">IRAC, ILAC, and advanced techniques for problem and essay questions</p>
              </div>
              <div className="bg-gradient-to-br from-purple-50 to-pink-50 p-6 rounded-xl border-2 border-purple-200">
                <ShoppingCart className="w-10 h-10 text-purple-600 mb-3" />
                <h3 className="text-xl font-bold text-slate-900 mb-2">Premium Study Notes</h3>
                <p className="text-slate-700">Affordable notes and custom question answers available for purchase</p>
              </div>
            </div>
          </div>
        </section>

        {/* Qualifying Degree Section */}
        <section className="mb-20">
          <div className="bg-gradient-to-r from-amber-50 to-orange-50 rounded-3xl shadow-xl p-8 md:p-12 border-l-8 border-amber-500">
            <div className="flex items-start gap-4">
              <AlertCircle className="w-10 h-10 text-amber-600 flex-shrink-0 mt-1" />
              <div>
                <h2 className="text-3xl font-bold text-slate-900 mb-4">Understanding Qualifying Degrees</h2>
                <p className="text-lg text-slate-800 leading-relaxed">
                  For a University of London LLB, the key thing to understand is that while subjects like <span className="font-semibold">Tort Law, Property Law, and European Union Law</span> form part of the traditional core of a Qualifying Law Degree, your choice of optional modules does not determine whether you can become a lawyer. Entry into the Solicitors Qualifying Examination or the Bar is based on passing professional training stages, not specific module selection.
                </p>
                <p className="text-lg text-slate-800 leading-relaxed mt-4">
                  However, choosing academically strong and relevant modules can give you a real advantage in legal understanding, exam performance, and future preparation, even though it is not a strict requirement.
                </p>
              </div>
            </div>
          </div>
        </section>

        {/* Modules Section */}
        <section id="modules" className="mb-20">
          <h2 className="text-5xl font-bold text-slate-900 mb-8 text-center">Module Directory</h2>
          
          {Object.entries(levels).map(([levelKey, level]) => (
            <div key={levelKey} className="mb-8">
              <button
                onClick={() => setExpandedLevel(expandedLevel === levelKey ? null : levelKey)}
                className="w-full bg-gradient-to-r from-blue-600 to-indigo-600 text-white p-6 rounded-2xl shadow-xl hover:shadow-2xl transition-all duration-300 flex items-center justify-between group"
              >
                <div className="text-left">
                  <h3 className="text-3xl font-bold">{level.title}</h3>
                  <p className="text-blue-100 mt-1">{level.price}</p>
                </div>
                <ChevronDown className={`w-8 h-8 transition-transform duration-300 ${expandedLevel === levelKey ? 'rotate-180' : ''}`} />
              </button>

              {expandedLevel === levelKey && (
                <div className="mt-4 space-y-4 animate-fadeIn">
                  {level.modules.map((module, idx) => (
                    <div key={idx} className="bg-white rounded-2xl shadow-lg overflow-hidden border-l-4 border-blue-500">
                      <button
                        onClick={() => setExpandedModule(expandedModule === `${levelKey}-${idx}` ? null : `${levelKey}-${idx}`)}
                        className="w-full p-6 text-left hover:bg-slate-50 transition-colors duration-200 flex items-center justify-between"
                      >
                        <div className="flex-1">
                          <div className="flex items-center gap-3 mb-2">
                            <span className="px-3 py-1 bg-blue-100 text-blue-800 rounded-full text-sm font-semibold">
                              {module.code}
                            </span>
                            {module.required && (
                              <span className="px-3 py-1 bg-green-100 text-green-800 rounded-full text-sm font-semibold">
                                Required
                              </span>
                            )}
                            {module.optional && (
                              <span className="px-3 py-1 bg-amber-100 text-amber-800 rounded-full text-sm font-semibold">
                                Optional
                              </span>
                            )}
                          </div>
                          <h4 className="text-2xl font-bold text-slate-900">{module.name}</h4>
                        </div>
                        <ChevronDown className={`w-6 h-6 text-slate-600 transition-transform duration-300 ${expandedModule === `${levelKey}-${idx}` ? 'rotate-180' : ''}`} />
                      </button>

                      {expandedModule === `${levelKey}-${idx}` && (
                        <div className="p-6 bg-slate-50 border-t border-slate-200">
                          <div className="mb-4">
                            <h5 className="text-lg font-bold text-slate-900 mb-2">📋 Exam Pattern:</h5>
                            <p className="text-slate-700 leading-relaxed">{module.pattern}</p>
                            {module.note && (
                              <p className="text-amber-700 mt-2 italic">{module.note}</p>
                            )}
                          </div>
                          
                          {module.topics.length > 0 && (
                            <div>
                              <h5 className="text-lg font-bold text-slate-900 mb-3">🎯 Important Topics:</h5>
                              <ul className="space-y-2">
                                {module.topics.map((topic, topicIdx) => (
                                  <li key={topicIdx} className="flex items-start gap-2">
                                    <span className="text-blue-600 mt-1">▸</span>
                                    <span className="text-slate-700">{topic}</span>
                                  </li>
                                ))}
                              </ul>
                            </div>
                          )}
                        </div>
                      )}
                    </div>
                  ))}
                </div>
              )}
            </div>
          ))}
        </section>

        {/* Exam Guidance Section */}
        <section id="exam-guidance" className="mb-20">
          <h2 className="text-5xl font-bold text-slate-900 mb-8 text-center">Exam Guidance & Techniques</h2>
          
          <div className="grid lg:grid-cols-2 gap-8">
            {/* Problem Questions */}
            <div className="bg-white rounded-3xl shadow-2xl p-8 border-t-4 border-green-500">
              <h3 className="text-3xl font-bold text-slate-900 mb-6">⚖️ Problem Questions</h3>
              
              <div className="space-y-6">
                <div>
                  <h4 className="text-2xl font-bold text-green-700 mb-3">IRAC Method</h4>
                  <div className="space-y-4">
                    <div className="bg-green-50 p-4 rounded-xl">
                      <h5 className="font-bold text-slate-900 mb-2">I - Issue</h5>
                      <p className="text-slate-700 mb-2">Identify the legal question precisely</p>
                      <p className="text-sm text-slate-600">❌ "Is there a trust?"</p>
                      <p className="text-sm text-green-700">✅ "Whether the wording satisfies certainty of intention for a valid express trust"</p>
                    </div>
                    
                    <div className="bg-green-50 p-4 rounded-xl">
                      <h5 className="font-bold text-slate-900 mb-2">R - Rule</h5>
                      <p className="text-slate-700">State the relevant legal principle with leading case authority and any tests or standards</p>
                    </div>
                    
                    <div className="bg-green-50 p-4 rounded-xl border-2 border-green-500">
                      <h5 className="font-bold text-slate-900 mb-2">A - Application (MOST IMPORTANT)</h5>
                      <p className="text-slate-700 mb-2">Apply the rule directly to the facts. Use comparisons with case facts and logical reasoning.</p>
                      <p className="text-sm font-semibold text-green-700">This is where most marks are won or lost.</p>
                    </div>
                    
                    <div className="bg-green-50 p-4 rounded-xl">
                      <h5 className="font-bold text-slate-900 mb-2">C - Conclusion</h5>
                      <p className="text-slate-700">Give a clear, reasoned answer. Avoid vague conclusions like "it depends"</p>
                    </div>
                  </div>
                </div>

                <div className="bg-blue-50 p-6 rounded-xl border-2 border-blue-400">
                  <h4 className="text-xl font-bold text-blue-900 mb-3">🔥 Advanced Tips</h4>
                  <ul className="space-y-2 text-slate-700">
                    <li><strong>ILAC:</strong> Issue - Law - Application - Conclusion (more depth)</li>
                    <li><strong>MIRAT:</strong> Material Facts - Issue - Rule - Application - Tentative Conclusion</li>
                    <li><strong>Key Rule:</strong> "Apply, Don't Recite" - Link every principle to facts</li>
                    <li><strong>Issue-Spotting:</strong> Identify ALL possible legal issues</li>
                    <li><strong>Layered Application:</strong> Main rule → Exceptions → Alternative outcomes</li>
                  </ul>
                </div>

                <div className="bg-red-50 p-6 rounded-xl border-2 border-red-400">
                  <h4 className="text-xl font-bold text-red-900 mb-3">⚠️ Common Mistakes to Avoid</h4>
                  <ul className="space-y-2 text-slate-700">
                    <li>❌ Writing long introductions</li>
                    <li>❌ Explaining law with no application</li>
                    <li>❌ Mixing multiple issues in one paragraph</li>
                    <li>❌ No clear conclusions</li>
                    <li>❌ Case dumping without relevance</li>
                  </ul>
                </div>
              </div>
            </div>

            {/* Essay Questions */}
            <div className="bg-white rounded-3xl shadow-2xl p-8 border-t-4 border-purple-500">
              <h3 className="text-3xl font-bold text-slate-900 mb-6">📝 Essay Questions</h3>
              
              <div className="space-y-4">
                <div className="bg-purple-50 p-5 rounded-xl">
                  <h4 className="font-bold text-purple-900 mb-2">"Discuss"</h4>
                  <p className="text-slate-700 text-sm">Present multiple perspectives, explain accurately, engage in analysis (not just description), reach a reasoned conclusion</p>
                </div>

                <div className="bg-purple-50 p-5 rounded-xl">
                  <h4 className="font-bold text-purple-900 mb-2">"To What Extent"</h4>
                  <p className="text-slate-700 text-sm mb-2">Explicitly evaluative - "How far is this statement true?"</p>
                  <p className="text-slate-600 text-sm">Structure: Argument FOR → Argument AGAINST → Final judgment</p>
                </div>

                <div className="bg-purple-50 p-5 rounded-xl border-2 border-purple-500">
                  <h4 className="font-bold text-purple-900 mb-2">"Critically Analyse / Critically Evaluate"</h4>
                  <p className="text-slate-700 text-sm mb-2">High-level writing (2:1 / First class territory)</p>
                  <p className="text-slate-600 text-sm">Assess: Effectiveness, Fairness, Consistency, Policy implications</p>
                  <p className="text-slate-600 text-sm mt-1">Include: Case law + academic opinion + judicial criticism + your reasoned stance</p>
                </div>

                <div className="bg-purple-50 p-5 rounded-xl">
                  <h4 className="font-bold text-purple-900 mb-2">"Assess"</h4>
                  <p className="text-slate-700 text-sm">Measure strengths and weaknesses, reach a clear judgment</p>
                </div>

                <div className="bg-purple-50 p-5 rounded-xl">
                  <h4 className="font-bold text-purple-900 mb-2">"Explain"</h4>
                  <p className="text-slate-700 text-sm">Provide clear, accurate account. Focus on legal principles and rules. Minimal evaluation required unless implied</p>
                </div>

                <div className="bg-purple-50 p-5 rounded-xl">
                  <h4 className="font-bold text-purple-900 mb-2">"Analyse"</h4>
                  <p className="text-slate-700 text-sm">Between explanation and critique. Break down into parts, show how principles interact, identify underlying reasoning</p>
                </div>

                <div className="bg-purple-50 p-5 rounded-xl">
                  <h4 className="font-bold text-purple-900 mb-2">"Consider"</h4>
                  <p className="text-slate-700 text-sm">Softer "discuss". Explore arguments, no strict conclusion requirement but still expected at UoL level</p>
                </div>

                <div className="bg-purple-50 p-5 rounded-xl">
                  <h4 className="font-bold text-purple-900 mb-2">"Evaluate"</h4>
                  <p className="text-slate-700 text-sm">Judge value or success. Requires criteria (fairness, certainty, efficiency)</p>
                </div>
              </div>
            </div>
          </div>
        </section>

        {/* Purchase Section */}
        <section id="purchase" className="mb-20">
          <div className="bg-gradient-to-br from-green-50 to-emerald-50 rounded-3xl shadow-2xl p-8 md:p-12 border-t-4 border-green-600">
            <div className="flex items-center gap-4 mb-8">
              <ShoppingCart className="w-12 h-12 text-green-600" />
              <h2 className="text-5xl font-bold text-slate-900">Purchase Study Materials</h2>
            </div>
            
            <div className="bg-gradient-to-r from-blue-600 to-indigo-600 text-white p-6 rounded-2xl mb-8 text-center">
              <p className="text-2xl font-bold">✅ Get structured, exam-ready answers for UoL papers</p>
            </div>

            {/* Module Notes Tiers */}
            <div className="mb-12">
              <h3 className="text-3xl font-bold text-slate-900 mb-6">📚 Module Notes</h3>
              
              <div className="grid lg:grid-cols-1 gap-6">
                {/* Tier 1 - Basic */}
                <div className="bg-white rounded-2xl shadow-xl overflow-hidden border-l-8 border-green-500">
                  <div className="bg-gradient-to-r from-green-500 to-emerald-500 text-white p-6">
                    <h4 className="text-2xl font-bold mb-2">🟢 TIER 1: BASIC (Entry Level)</h4>
                    <p className="text-green-100">For students who just want cheap help to pass</p>
                  </div>
                  <div className="p-6">
                    <div className="mb-4">
                      <h5 className="font-bold text-slate-900 mb-3">Includes:</h5>
                      <ul className="space-y-2 text-slate-700">
                        <li className="flex items-start gap-2">
                          <span className="text-green-600 mt-1">✓</span>
                          <span>Concise exam-focused notes</span>
                        </li>
                        <li className="flex items-start gap-2">
                          <span className="text-green-600 mt-1">✓</span>
                          <span>Key topics only (no deep explanations)</span>
                        </li>
                        <li className="flex items-start gap-2">
                          <span className="text-green-600 mt-1">✓</span>
                          <span>Bullet-point summaries</span>
                        </li>
                      </ul>
                    </div>
                    <div className="grid grid-cols-3 gap-4 mt-6">
                      <div className="bg-blue-50 p-4 rounded-xl text-center">
                        <p className="text-sm text-slate-600 mb-1">Level 4</p>
                        <p className="text-2xl font-bold text-blue-600">PKR 1,500</p>
                      </div>
                      <div className="bg-indigo-50 p-4 rounded-xl text-center">
                        <p className="text-sm text-slate-600 mb-1">Level 5</p>
                        <p className="text-2xl font-bold text-indigo-600">PKR 2,500</p>
                      </div>
                      <div className="bg-purple-50 p-4 rounded-xl text-center">
                        <p className="text-sm text-slate-600 mb-1">Level 6</p>
                        <p className="text-2xl font-bold text-purple-600">PKR 3,500</p>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>

            {/* Question Answers Tiers */}
            <div className="mb-12">
              <h3 className="text-3xl font-bold text-slate-900 mb-6">❓ Paid Answers Model</h3>
              
              <div className="space-y-6">
                {/* Tier 1 - Basic Answer */}
                <div className="bg-white rounded-2xl shadow-xl overflow-hidden border-l-8 border-green-500">
                  <div className="bg-gradient-to-r from-green-500 to-emerald-500 text-white p-6">
                    <h4 className="text-2xl font-bold mb-2">🟢 TIER 1: BASIC ANSWER</h4>
                    <p className="text-green-100">For students who just want something to submit/pass</p>
                  </div>
                  <div className="p-6">
                    <div className="mb-4">
                      <h5 className="font-bold text-slate-900 mb-3">Includes:</h5>
                      <ul className="space-y-2 text-slate-700">
                        <li className="flex items-start gap-2">
                          <span className="text-green-600 mt-1">✓</span>
                          <span>Direct answer</span>
                        </li>
                        <li className="flex items-start gap-2">
                          <span className="text-green-600 mt-1">✓</span>
                          <span>Basic structure</span>
                        </li>
                        <li className="flex items-start gap-2">
                          <span className="text-green-600 mt-1">✓</span>
                          <span>Minimal case law</span>
                        </li>
                        <li className="flex items-start gap-2">
                          <span className="text-green-600 mt-1">✓</span>
                          <span>600–900 words</span>
                        </li>
                      </ul>
                    </div>
                    <div className="grid grid-cols-3 gap-4 mt-6">
                      <div className="bg-green-50 p-4 rounded-xl text-center">
                        <p className="text-sm text-slate-600 mb-1">Level 4</p>
                        <p className="text-2xl font-bold text-green-600">PKR 500</p>
                      </div>
                      <div className="bg-green-50 p-4 rounded-xl text-center">
                        <p className="text-sm text-slate-600 mb-1">Level 5</p>
                        <p className="text-2xl font-bold text-green-600">PKR 700</p>
                      </div>
                      <div className="bg-green-50 p-4 rounded-xl text-center">
                        <p className="text-sm text-slate-600 mb-1">Level 6</p>
                        <p className="text-2xl font-bold text-green-600">PKR 1,000</p>
                      </div>
                    </div>
                    <p className="text-center text-slate-600 mt-4 font-semibold">👉 "Simple Pass Answer"</p>
                  </div>
                </div>

                {/* Tier 2 - Standard Answer (Best Seller) */}
                <div className="bg-white rounded-2xl shadow-xl overflow-hidden border-l-8 border-blue-500 ring-4 ring-blue-200">
                  <div className="bg-gradient-to-r from-blue-500 to-indigo-500 text-white p-6">
                    <div className="flex items-center justify-between">
                      <div>
                        <h4 className="text-2xl font-bold mb-2">🔵 TIER 2: STANDARD ANSWER</h4>
                        <p className="text-blue-100">This should be your main offering</p>
                      </div>
                      <span className="bg-yellow-400 text-yellow-900 px-4 py-2 rounded-full font-bold text-sm">BEST SELLER 💰</span>
                    </div>
                  </div>
                  <div className="p-6">
                    <div className="mb-4">
                      <h5 className="font-bold text-slate-900 mb-3">Includes:</h5>
                      <ul className="space-y-2 text-slate-700">
                        <li className="flex items-start gap-2">
                          <span className="text-blue-600 mt-1">✓</span>
                          <span>Proper IRAC / essay structure</span>
                        </li>
                        <li className="flex items-start gap-2">
                          <span className="text-blue-600 mt-1">✓</span>
                          <span>Relevant case law</span>
                        </li>
                        <li className="flex items-start gap-2">
                          <span className="text-blue-600 mt-1">✓</span>
                          <span>Clear arguments + application</span>
                        </li>
                        <li className="flex items-start gap-2">
                          <span className="text-blue-600 mt-1">✓</span>
                          <span>900–1,500 words</span>
                        </li>
                      </ul>
                    </div>
                    <div className="grid grid-cols-3 gap-4 mt-6">
                      <div className="bg-blue-50 p-4 rounded-xl text-center border-2 border-blue-300">
                        <p className="text-sm text-slate-600 mb-1">Level 4</p>
                        <p className="text-2xl font-bold text-blue-600">PKR 1,000</p>
                      </div>
                      <div className="bg-blue-50 p-4 rounded-xl text-center border-2 border-blue-300">
                        <p className="text-sm text-slate-600 mb-1">Level 5</p>
                        <p className="text-2xl font-bold text-blue-600">PKR 1,500</p>
                      </div>
                      <div className="bg-blue-50 p-4 rounded-xl text-center border-2 border-blue-300">
                        <p className="text-sm text-slate-600 mb-1">Level 6</p>
                        <p className="text-2xl font-bold text-blue-600">PKR 2,000</p>
                      </div>
                    </div>
                    <p className="text-center text-slate-600 mt-4 font-semibold">👉 "Exam-Ready Answer"</p>
                  </div>
                </div>

                {/* Tier 3 - Premium Answer */}
                <div className="bg-white rounded-2xl shadow-xl overflow-hidden border-l-8 border-red-500">
                  <div className="bg-gradient-to-r from-red-500 to-orange-500 text-white p-6">
                    <div className="flex items-center justify-between">
                      <div>
                        <h4 className="text-2xl font-bold mb-2">🔴 TIER 3: PREMIUM ANSWER</h4>
                        <p className="text-red-100">For serious students aiming higher marks</p>
                      </div>
                      <span className="bg-white text-red-600 px-4 py-2 rounded-full font-bold text-sm">HIGH VALUE 🔥</span>
                    </div>
                  </div>
                  <div className="p-6">
                    <div className="mb-4">
                      <h5 className="font-bold text-slate-900 mb-3">Includes:</h5>
                      <ul className="space-y-2 text-slate-700">
                        <li className="flex items-start gap-2">
                          <span className="text-red-600 mt-1">✓</span>
                          <span>Everything in Standard</span>
                        </li>
                        <li className="flex items-start gap-2">
                          <span className="text-red-600 mt-1">✓</span>
                          <span>Strong case law integration</span>
                        </li>
                        <li className="flex items-start gap-2">
                          <span className="text-red-600 mt-1">✓</span>
                          <span>Critical analysis + evaluation</span>
                        </li>
                        <li className="flex items-start gap-2">
                          <span className="text-red-600 mt-1">✓</span>
                          <span>Polished structure (First-class style)</span>
                        </li>
                        <li className="flex items-start gap-2">
                          <span className="text-red-600 mt-1">✓</span>
                          <span>1,500–2,500 words</span>
                        </li>
                      </ul>
                    </div>
                    <div className="grid grid-cols-3 gap-4 mt-6">
                      <div className="bg-red-50 p-4 rounded-xl text-center">
                        <p className="text-sm text-slate-600 mb-1">Level 4</p>
                        <p className="text-2xl font-bold text-red-600">PKR 1,500</p>
                      </div>
                      <div className="bg-red-50 p-4 rounded-xl text-center">
                        <p className="text-sm text-slate-600 mb-1">Level 5</p>
                        <p className="text-2xl font-bold text-red-600">PKR 2,500</p>
                      </div>
                      <div className="bg-red-50 p-4 rounded-xl text-center">
                        <p className="text-sm text-slate-600 mb-1">Level 6</p>
                        <p className="text-2xl font-bold text-red-600">PKR 3,500</p>
                      </div>
                    </div>
                    <p className="text-center text-slate-600 mt-4 font-semibold">👉 "High-Scoring Model Answer"</p>
                  </div>
                </div>
              </div>
            </div>

            {/* Bundle Pricing */}
            <div className="mb-12">
              <h3 className="text-3xl font-bold text-slate-900 mb-6">📦 Bundle Pricing</h3>
              
              <div className="grid md:grid-cols-3 gap-6">
                {/* 4 Answers Pack */}
                <div className="bg-white rounded-2xl shadow-lg p-6 border-t-4 border-purple-500">
                  <h4 className="text-xl font-bold text-slate-900 mb-4">🔹 4 Answers Pack</h4>
                  <div className="space-y-3">
                    <div className="flex justify-between items-center p-3 bg-purple-50 rounded-lg">
                      <span className="text-slate-700">Level 4</span>
                      <span className="font-bold text-purple-600">PKR 2,500</span>
                    </div>
                    <div className="flex justify-between items-center p-3 bg-purple-50 rounded-lg">
                      <span className="text-slate-700">Level 5</span>
                      <span className="font-bold text-purple-600">PKR 4,000</span>
                    </div>
                    <div className="flex justify-between items-center p-3 bg-purple-50 rounded-lg">
                      <span className="text-slate-700">Level 6</span>
                      <span className="font-bold text-purple-600">PKR 6,000</span>
                    </div>
                  </div>
                </div>

                {/* 6 Answers Pack - Best Value */}
                <div className="bg-white rounded-2xl shadow-lg p-6 border-t-4 border-yellow-500 ring-4 ring-yellow-200">
                  <div className="flex items-center justify-between mb-4">
                    <h4 className="text-xl font-bold text-slate-900">🔹 6 Answers Pack</h4>
                    <span className="bg-yellow-400 text-yellow-900 px-2 py-1 rounded-full text-xs font-bold">BEST VALUE</span>
                  </div>
                  <div className="space-y-3">
                    <div className="flex justify-between items-center p-3 bg-yellow-50 rounded-lg border-2 border-yellow-300">
                      <span className="text-slate-700">Level 4</span>
                      <span className="font-bold text-yellow-700">PKR 4,000</span>
                    </div>
                    <div className="flex justify-between items-center p-3 bg-yellow-50 rounded-lg border-2 border-yellow-300">
                      <span className="text-slate-700">Level 5</span>
                      <span className="font-bold text-yellow-700">PKR 6,500</span>
                    </div>
                    <div className="flex justify-between items-center p-3 bg-yellow-50 rounded-lg border-2 border-yellow-300">
                      <span className="text-slate-700">Level 6</span>
                      <span className="font-bold text-yellow-700">PKR 10,000</span>
                    </div>
                  </div>
                </div>

                {/* 10 Answers Pack */}
                <div className="bg-white rounded-2xl shadow-lg p-6 border-t-4 border-indigo-500">
                  <h4 className="text-xl font-bold text-slate-900 mb-4">🔹 10 Answers Pack</h4>
                  <div className="space-y-3">
                    <div className="flex justify-between items-center p-3 bg-indigo-50 rounded-lg">
                      <span className="text-slate-700">Level 4</span>
                      <span className="font-bold text-indigo-600">PKR 7,500</span>
                    </div>
                    <div className="flex justify-between items-center p-3 bg-indigo-50 rounded-lg">
                      <span className="text-slate-700">Level 5</span>
                      <span className="font-bold text-indigo-600">PKR 12,000</span>
                    </div>
                    <div className="flex justify-between items-center p-3 bg-indigo-50 rounded-lg">
                      <span className="text-slate-700">Level 6</span>
                      <span className="font-bold text-indigo-600">PKR 18,000</span>
                    </div>
                  </div>
                </div>
              </div>
            </div>

            {/* Add-Ons */}
            <div className="mb-12">
              <h3 className="text-3xl font-bold text-slate-900 mb-6">💸 Add-Ons (Upsell)</h3>
              
              <div className="grid md:grid-cols-2 gap-6">
                <div className="bg-white p-6 rounded-2xl shadow-lg border-l-4 border-orange-500">
                  <h4 className="text-xl font-bold text-slate-900 mb-3">⚡ Urgent Delivery (12–24 hrs)</h4>
                  <p className="text-3xl font-bold text-orange-600">PKR 500 – 1,000</p>
                </div>
                <div className="bg-white p-6 rounded-2xl shadow-lg border-l-4 border-pink-500">
                  <h4 className="text-xl font-bold text-slate-900 mb-3">✍️ Extra Length / Deep Analysis</h4>
                  <p className="text-3xl font-bold text-pink-600">PKR 500 – 1,500</p>
                </div>
              </div>
            </div>

            {/* Important Rules */}
            <div className="bg-red-50 p-6 rounded-2xl border-2 border-red-300 mb-8">
              <h3 className="text-xl font-bold text-red-900 mb-4">⚠️ IMPORTANT RULES</h3>
              <ul className="space-y-2 text-slate-700">
                <li className="flex items-start gap-2">
                  <span className="text-red-600 mt-1">⛔</span>
                  <span>Word limit per tier must be respected</span>
                </li>
                <li className="flex items-start gap-2">
                  <span className="text-red-600 mt-1">⛔</span>
                  <span>Standard delivery time: 24–48 hours</span>
                </li>
                <li className="flex items-start gap-2">
                  <span className="text-red-600 mt-1">⛔</span>
                  <span>Extra charges apply for urgent work</span>
                </li>
              </ul>
            </div>

            {/* Order Form for Notes */}
            <form action="https://formspree.io/f/mqenoeov" method="POST" className="bg-white p-8 rounded-2xl shadow-xl mb-8">
              <h3 className="text-2xl font-bold text-slate-900 mb-6">📝 Order Notes</h3>
              
              <div className="space-y-4">
                <div>
                  <label className="block text-slate-900 font-semibold mb-2">Your Name</label>
                  <input
                    type="text"
                    name="name"
                    required
                    className="w-full px-4 py-3 border-2 border-slate-300 rounded-xl focus:border-green-500 focus:ring-2 focus:ring-green-200 outline-none transition-all"
                    placeholder="Enter your full name"
                  />
                </div>

                <div>
                  <label className="block text-slate-900 font-semibold mb-2">Email Address</label>
                  <input
                    type="email"
                    name="email"
                    required
                    className="w-full px-4 py-3 border-2 border-slate-300 rounded-xl focus:border-green-500 focus:ring-2 focus:ring-green-200 outline-none transition-all"
                    placeholder="your.email@example.com"
                  />
                </div>

                <div>
                  <label className="block text-slate-900 font-semibold mb-2">Level</label>
                  <select
                    name="level"
                    required
                    className="w-full px-4 py-3 border-2 border-slate-300 rounded-xl focus:border-green-500 focus:ring-2 focus:ring-green-200 outline-none transition-all"
                  >
                    <option value="">Select Level</option>
                    <option value="level4">Level 4</option>
                    <option value="level5">Level 5</option>
                    <option value="level6">Level 6</option>
                  </select>
                </div>

                <div>
                  <label className="block text-slate-900 font-semibold mb-2">Module Name</label>
                  <input
                    type="text"
                    name="module"
                    required
                    className="w-full px-4 py-3 border-2 border-slate-300 rounded-xl focus:border-green-500 focus:ring-2 focus:ring-green-200 outline-none transition-all"
                    placeholder="e.g., Contract Law, Tort Law, etc."
                  />
                </div>

                <div>
                  <label className="block text-slate-900 font-semibold mb-2">Additional Information</label>
                  <textarea
                    name="additional_info"
                    rows="3"
                    className="w-full px-4 py-3 border-2 border-slate-300 rounded-xl focus:border-green-500 focus:ring-2 focus:ring-green-200 outline-none transition-all"
                    placeholder="Any additional details or special requests..."
                  ></textarea>
                </div>

                <button
                  type="submit"
                  className="w-full bg-gradient-to-r from-green-600 to-emerald-600 text-white py-4 rounded-xl font-bold text-lg hover:shadow-2xl transform hover:scale-[1.02] transition-all duration-300"
                >
                  Submit Notes Order
                </button>
              </div>
            </form>

            {/* Question Submission Form */}
            <form action="https://formspree.io/f/xgodbanw" method="POST" className="bg-white p-8 rounded-2xl shadow-xl">
              <h3 className="text-2xl font-bold text-slate-900 mb-6">❓ Submit Questions for Answers</h3>
              <p className="text-slate-600 mb-6">Submit up to 10 questions at once</p>
              
              <div className="space-y-4">
                <div>
                  <label className="block text-slate-900 font-semibold mb-2">Your Name</label>
                  <input
                    type="text"
                    name="name"
                    required
                    className="w-full px-4 py-3 border-2 border-slate-300 rounded-xl focus:border-blue-500 focus:ring-2 focus:ring-blue-200 outline-none transition-all"
                    placeholder="Enter your full name"
                  />
                </div>

                <div>
                  <label className="block text-slate-900 font-semibold mb-2">Email Address</label>
                  <input
                    type="email"
                    name="email"
                    required
                    className="w-full px-4 py-3 border-2 border-slate-300 rounded-xl focus:border-blue-500 focus:ring-2 focus:ring-blue-200 outline-none transition-all"
                    placeholder="your.email@example.com"
                  />
                </div>

                <div>
                  <label className="block text-slate-900 font-semibold mb-2">Level</label>
                  <select
                    name="level"
                    required
                    className="w-full px-4 py-3 border-2 border-slate-300 rounded-xl focus:border-blue-500 focus:ring-2 focus:ring-blue-200 outline-none transition-all"
                  >
                    <option value="">Select Level</option>
                    <option value="level4">Level 4</option>
                    <option value="level5">Level 5</option>
                    <option value="level6">Level 6</option>
                  </select>
                </div>

                <div>
                  <label className="block text-slate-900 font-semibold mb-2">Answer Tier</label>
                  <select
                    name="answer_tier"
                    required
                    className="w-full px-4 py-3 border-2 border-slate-300 rounded-xl focus:border-blue-500 focus:ring-2 focus:ring-blue-200 outline-none transition-all"
                  >
                    <option value="">Select Tier</option>
                    <option value="basic">Basic Answer (Simple Pass)</option>
                    <option value="standard">Standard Answer (Exam-Ready) - BEST SELLER</option>
                    <option value="premium">Premium Answer (High-Scoring)</option>
                  </select>
                </div>

                <div>
                  <label className="block text-slate-900 font-semibold mb-2">Bundle or Single Question</label>
                  <select
                    name="bundle_type"
                    required
                    className="w-full px-4 py-3 border-2 border-slate-300 rounded-xl focus:border-blue-500 focus:ring-2 focus:ring-blue-200 outline-none transition-all"
                  >
                    <option value="">Select Option</option>
                    <option value="single">Single Question</option>
                    <option value="bundle-4">4 Answers Pack</option>
                    <option value="bundle-6">6 Answers Pack (BEST VALUE)</option>
                    <option value="bundle-10">10 Answers Pack</option>
                  </select>
                </div>

                <div>
                  <label className="block text-slate-900 font-semibold mb-2">Module Name(s)</label>
                  <input
                    type="text"
                    name="modules"
                    required
                    className="w-full px-4 py-3 border-2 border-slate-300 rounded-xl focus:border-blue-500 focus:ring-2 focus:ring-blue-200 outline-none transition-all"
                    placeholder="e.g., Contract Law, Tort Law, etc."
                  />
                </div>

                <div>
                  <label className="block text-slate-900 font-semibold mb-2">Your Question(s)</label>
                  <textarea
                    name="questions"
                    required
                    rows="8"
                    className="w-full px-4 py-3 border-2 border-slate-300 rounded-xl focus:border-blue-500 focus:ring-2 focus:ring-blue-200 outline-none transition-all"
                    placeholder="Paste your question(s) here. If multiple questions, number them (1, 2, 3, etc.). Maximum 10 questions per submission."
                  ></textarea>
                </div>

                <div>
                  <label className="block text-slate-900 font-semibold mb-2">Add-Ons (Optional)</label>
                  <div className="space-y-2">
                    <label className="flex items-center gap-2">
                      <input type="checkbox" name="urgent_delivery" value="yes" className="w-4 h-4 text-blue-600" />
                      <span className="text-slate-700">Urgent Delivery (12-24 hrs) - PKR 500-1,000</span>
                    </label>
                    <label className="flex items-center gap-2">
                      <input type="checkbox" name="extra_analysis" value="yes" className="w-4 h-4 text-blue-600" />
                      <span className="text-slate-700">Extra Length / Deep Analysis - PKR 500-1,500</span>
                    </label>
                  </div>
                </div>

                <div>
                  <label className="block text-slate-900 font-semibold mb-2">Additional Instructions</label>
                  <textarea
                    name="additional_instructions"
                    rows="3"
                    className="w-full px-4 py-3 border-2 border-slate-300 rounded-xl focus:border-blue-500 focus:ring-2 focus:ring-blue-200 outline-none transition-all"
                    placeholder="Any specific requirements or preferences..."
                  ></textarea>
                </div>

                <button
                  type="submit"
                  className="w-full bg-gradient-to-r from-blue-600 to-indigo-600 text-white py-4 rounded-xl font-bold text-lg hover:shadow-2xl transform hover:scale-[1.02] transition-all duration-300"
                >
                  Submit Question(s) for Answers
                </button>
              </div>
            </form>
          </div>
        </section>

        {/* About Section */}
        <section id="about" className="mb-20">
          <div className="bg-gradient-to-br from-blue-50 to-indigo-50 rounded-3xl shadow-2xl p-8 md:p-12 border-t-4 border-blue-600">
            <div className="flex items-center gap-4 mb-6">
              <User className="w-12 h-12 text-blue-600" />
              <h2 className="text-5xl font-bold text-slate-900">About the Founder</h2>
            </div>
            
            <div className="bg-white p-8 rounded-2xl shadow-lg">
              <p className="text-lg text-slate-700 leading-relaxed mb-6">
                This platform was created by a University of London LLB graduate who understands the challenges faced by students navigating this demanding program. Having experienced the difficulties firsthand, the founder is committed to providing comprehensive guidance and resources to help current students achieve their academic goals.
              </p>
              
              <div className="bg-blue-50 p-6 rounded-xl border-2 border-blue-200">
                <h3 className="text-xl font-bold text-slate-900 mb-4">Mission Statement</h3>
                <p className="text-slate-700 leading-relaxed">
                  To better guide University of London LLB students so they don't have to face the same problems and uncertainties. By sharing structured exam guidance, important topics, and affordable study materials, this platform aims to empower students at all levels to excel in their studies and confidently approach their examinations.
                </p>
              </div>

              <div className="mt-8 p-6 bg-gradient-to-r from-green-50 to-emerald-50 rounded-xl border-2 border-green-300">
                <h3 className="text-xl font-bold text-slate-900 mb-4">📞 Contact Information</h3>
                <div className="flex items-center gap-3">
                  <Mail className="w-6 h-6 text-green-600" />
                  <a href="mailto:umairahmad7643@gmail.com" className="text-lg text-green-700 hover:text-green-900 font-semibold hover:underline transition-colors">
                    umairahmad7643@gmail.com
                  </a>
                </div>
                <p className="text-slate-600 mt-3 text-sm">
                  For Francis Ng articles (Tort Law & Equity and Trusts), contact via the email above.
                </p>
              </div>
            </div>
          </div>
        </section>

        {/* Complaints Section */}
        <section id="complaints" className="mb-20">
          <div className="bg-gradient-to-br from-red-50 to-orange-50 rounded-3xl shadow-2xl p-8 md:p-12 border-t-4 border-red-600">
            <div className="flex items-center gap-4 mb-6">
              <MessageSquare className="w-12 h-12 text-red-600" />
              <h2 className="text-5xl font-bold text-slate-900">Submit a Complaint</h2>
            </div>
            
            <p className="text-lg text-slate-700 mb-8">
              If you've found any errors or inaccuracies regarding any module information on this website, please let us know. Your feedback helps us maintain the quality and accuracy of our resources.
            </p>

            <form action="https://formspree.io/f/mwvyjvdn" method="POST" className="bg-white p-8 rounded-2xl shadow-xl">
              <div className="space-y-4">
                <div>
                  <label className="block text-slate-900 font-semibold mb-2">Your Name</label>
                  <input
                    type="text"
                    name="name"
                    required
                    className="w-full px-4 py-3 border-2 border-slate-300 rounded-xl focus:border-red-500 focus:ring-2 focus:ring-red-200 outline-none transition-all"
                    placeholder="Enter your name"
                  />
                </div>

                <div>
                  <label className="block text-slate-900 font-semibold mb-2">Email Address</label>
                  <input
                    type="email"
                    name="email"
                    required
                    className="w-full px-4 py-3 border-2 border-slate-300 rounded-xl focus:border-red-500 focus:ring-2 focus:ring-red-200 outline-none transition-all"
                    placeholder="your.email@example.com"
                  />
                </div>

                <div>
                  <label className="block text-slate-900 font-semibold mb-2">Module / Section</label>
                  <input
                    type="text"
                    name="module"
                    required
                    className="w-full px-4 py-3 border-2 border-slate-300 rounded-xl focus:border-red-500 focus:ring-2 focus:ring-red-200 outline-none transition-all"
                    placeholder="Which module or section has an error?"
                  />
                </div>

                <div>
                  <label className="block text-slate-900 font-semibold mb-2">Description of Error</label>
                  <textarea
                    name="complaint"
                    required
                    rows="6"
                    className="w-full px-4 py-3 border-2 border-slate-300 rounded-xl focus:border-red-500 focus:ring-2 focus:ring-red-200 outline-none transition-all"
                    placeholder="Please describe the error or issue in detail..."
                  ></textarea>
                </div>

                <button
                  type="submit"
                  className="w-full bg-gradient-to-r from-red-600 to-orange-600 text-white py-4 rounded-xl font-bold text-lg hover:shadow-2xl transform hover:scale-[1.02] transition-all duration-300"
                >
                  Submit Complaint
                </button>
              </div>
            </form>
          </div>
        </section>
      </main>

      {/* Footer */}
      <footer className="bg-gradient-to-r from-slate-900 via-blue-900 to-indigo-900 text-white py-12">
        <div className="container mx-auto px-4 text-center">
          <h3 className="text-2xl font-bold mb-2">UoL LLB Guide</h3>
          <p className="text-blue-200 mb-4">Empowering University of London LLB Students</p>
          <p className="text-sm text-blue-300">
            © 2024 UoL LLB Guide. Created to help students succeed in their legal education journey.
          </p>
          <div className="mt-6">
            <a href="mailto:umairahmad7643@gmail.com" className="inline-flex items-center gap-2 text-blue-200 hover:text-white transition-colors">
              <Mail className="w-5 h-5" />
              umairahmad7643@gmail.com
            </a>
          </div>
        </div>
      </footer>

      <style jsx>{`
        @keyframes fadeIn {
          from {
            opacity: 0;
            transform: translateY(-10px);
          }
          to {
            opacity: 1;
            transform: translateY(0);
          }
        }

        .animate-fadeIn {
          animation: fadeIn 0.3s ease-out;
        }
      `}</style>
    </div>
  );
}
