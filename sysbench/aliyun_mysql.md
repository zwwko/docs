





<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
  <link rel="dns-prefetch" href="https://github.githubassets.com">
  <link rel="dns-prefetch" href="https://avatars0.githubusercontent.com">
  <link rel="dns-prefetch" href="https://avatars1.githubusercontent.com">
  <link rel="dns-prefetch" href="https://avatars2.githubusercontent.com">
  <link rel="dns-prefetch" href="https://avatars3.githubusercontent.com">
  <link rel="dns-prefetch" href="https://github-cloud.s3.amazonaws.com">
  <link rel="dns-prefetch" href="https://user-images.githubusercontent.com/">



  <link crossorigin="anonymous" media="all" integrity="sha512-OBabailf0Gja8rWVZO1xyYAw//CQdLOJF4riG050gTxsVqVD7az4Sq56hPWfv3AoaxuEhYXgQlGQcNxzZzDyVA==" rel="stylesheet" href="https://github.githubassets.com/assets/frameworks-d69542a4a3958db914b3bec3f757de26.css" />
  <link crossorigin="anonymous" media="all" integrity="sha512-9f3NsOQR/iafpq5oTq9iaNzpmB3VaUcvR6AtzwqKitGWmnCnxlp4dfbENMlnj8IgKSCuwyrZTQ6Rok0xkfeiLA==" rel="stylesheet" href="https://github.githubassets.com/assets/site-e4d561c16b6b9aaadbf00c0559c20085.css" />
    <link crossorigin="anonymous" media="all" integrity="sha512-VbMsb0mu2JLbNapUCk1kAeQdtgtd5d2dVH76GGsqU5tx/7elhj3w/OJ15dzZm7NPgO4DIKPFzV6ONJBLs4ea+w==" rel="stylesheet" href="https://github.githubassets.com/assets/github-7ef5c996d78e15565f21408b8a456177.css" />
    
    
    
    

  <meta name="viewport" content="width=device-width">
  
  <title>docs-cn/sysbench.md at master · pingcap/docs-cn · GitHub</title>
    <meta name="description" content="TiDB/TiKV/PD documents in Chinese. Contribute to pingcap/docs-cn development by creating an account on GitHub.">
    <link rel="search" type="application/opensearchdescription+xml" href="/opensearch.xml" title="GitHub">
  <link rel="fluid-icon" href="https://github.com/fluidicon.png" title="GitHub">
  <meta property="fb:app_id" content="1401488693436528">

    <meta name="twitter:image:src" content="https://avatars1.githubusercontent.com/u/11855343?s=400&amp;v=4" /><meta name="twitter:site" content="@github" /><meta name="twitter:card" content="summary" /><meta name="twitter:title" content="pingcap/docs-cn" /><meta name="twitter:description" content="TiDB/TiKV/PD documents in Chinese. Contribute to pingcap/docs-cn development by creating an account on GitHub." />
    <meta property="og:image" content="https://avatars1.githubusercontent.com/u/11855343?s=400&amp;v=4" /><meta property="og:site_name" content="GitHub" /><meta property="og:type" content="object" /><meta property="og:title" content="pingcap/docs-cn" /><meta property="og:url" content="https://github.com/pingcap/docs-cn" /><meta property="og:description" content="TiDB/TiKV/PD documents in Chinese. Contribute to pingcap/docs-cn development by creating an account on GitHub." />

  <link rel="assets" href="https://github.githubassets.com/">
  
  <meta name="pjax-timeout" content="1000">
  
  <meta name="request-id" content="3BFF:4B8D:CFCFF:12D50B:5CC010B0" data-pjax-transient>


  

  <meta name="selected-link" value="repo_source" data-pjax-transient>

      <meta name="google-site-verification" content="KT5gs8h0wvaagLKAVWq8bbeNwnZZK1r1XQysX3xurLU">
    <meta name="google-site-verification" content="ZzhVyEFwb7w3e0-uOTltm8Jsck2F5StVihD0exw2fsA">
    <meta name="google-site-verification" content="GXs5KoUUkNCoaAZn7wPN-t01Pywp9M3sEjnt_3_ZWPc">

  <meta name="octolytics-host" content="collector.githubapp.com" /><meta name="octolytics-app-id" content="github" /><meta name="octolytics-event-url" content="https://collector.githubapp.com/github-external/browser_event" /><meta name="octolytics-dimension-request_id" content="3BFF:4B8D:CFCFF:12D50B:5CC010B0" /><meta name="octolytics-dimension-region_edge" content="ap-southeast-1" /><meta name="octolytics-dimension-region_render" content="iad" />
<meta name="analytics-location" content="/&lt;user-name&gt;/&lt;repo-name&gt;/blob/show" data-pjax-transient="true" />



    <meta name="google-analytics" content="UA-3769691-2">


<meta class="js-ga-set" name="dimension1" content="Logged Out">



  

      <meta name="hostname" content="github.com">
    <meta name="user-login" content="">

      <meta name="expected-hostname" content="github.com">
    <meta name="js-proxy-site-detection-payload" content="NmExOWM1OTU5NWNmNWYwMmQ2ZTBjZWFjZDdlNzkyNWMxNzkxYmRiODU1NTc1YjFkYjE1ODFhMzcyYWM5YTYzNXx7InJlbW90ZV9hZGRyZXNzIjoiNjAuMTkxLjExNC4yIiwicmVxdWVzdF9pZCI6IjNCRkY6NEI4RDpDRkNGRjoxMkQ1MEI6NUNDMDEwQjAiLCJ0aW1lc3RhbXAiOjE1NTYwOTEwNTcsImhvc3QiOiJnaXRodWIuY29tIn0=">

    <meta name="enabled-features" content="UNIVERSE_BANNER,MARKETPLACE_INVOICED_BILLING,MARKETPLACE_SOCIAL_PROOF_CUSTOMERS,MARKETPLACE_TRENDING_SOCIAL_PROOF,MARKETPLACE_RECOMMENDATIONS">

  <meta name="html-safe-nonce" content="14c448bd0abc94604697128e21baab3cd98deba8">

  <meta http-equiv="x-pjax-version" content="f94b77ea0bb076029326950344d5404c">
  

      <link href="https://github.com/pingcap/docs-cn/commits/master.atom" rel="alternate" title="Recent Commits to docs-cn:master" type="application/atom+xml">

  <meta name="go-import" content="github.com/pingcap/docs-cn git https://github.com/pingcap/docs-cn.git">

  <meta name="octolytics-dimension-user_id" content="11855343" /><meta name="octolytics-dimension-user_login" content="pingcap" /><meta name="octolytics-dimension-repository_id" content="64188788" /><meta name="octolytics-dimension-repository_nwo" content="pingcap/docs-cn" /><meta name="octolytics-dimension-repository_public" content="true" /><meta name="octolytics-dimension-repository_is_fork" content="false" /><meta name="octolytics-dimension-repository_network_root_id" content="64188788" /><meta name="octolytics-dimension-repository_network_root_nwo" content="pingcap/docs-cn" /><meta name="octolytics-dimension-repository_explore_github_marketplace_ci_cta_shown" content="false" />


    <link rel="canonical" href="https://github.com/pingcap/docs-cn/blob/master/benchmark/sysbench.md" data-pjax-transient>


  <meta name="browser-stats-url" content="https://api.github.com/_private/browser/stats">

  <meta name="browser-errors-url" content="https://api.github.com/_private/browser/errors">

  <link rel="mask-icon" href="https://github.githubassets.com/pinned-octocat.svg" color="#000000">
  <link rel="icon" type="image/x-icon" class="js-site-favicon" href="https://github.githubassets.com/favicon.ico">

<meta name="theme-color" content="#1e2327">




  <link rel="manifest" href="/manifest.json" crossOrigin="use-credentials">

  </head>

  <body class="logged-out env-production page-blob">
    

  <div class="position-relative js-header-wrapper ">
    <a href="#start-of-content" tabindex="1" class="px-2 py-4 bg-blue text-white show-on-focus js-skip-to-content">Skip to content</a>
    <div id="js-pjax-loader-bar" class="pjax-loader-bar"><div class="progress"></div></div>

    
    
    


        <header class="Header-old header-logged-out  position-relative f4 py-2" role="banner">
  <div class="container-lg d-flex px-3">
    <div class="d-flex flex-justify-between flex-items-center">
        <a class="mr-4" href="https://github.com/" aria-label="Homepage" data-ga-click="(Logged out) Header, go to homepage, icon:logo-wordmark">
          <svg height="32" class="octicon octicon-mark-github text-white" viewBox="0 0 16 16" version="1.1" width="32" aria-hidden="true"><path fill-rule="evenodd" d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0 0 16 8c0-4.42-3.58-8-8-8z"/></svg>
        </a>
    </div>

    <div class="HeaderMenu HeaderMenu--logged-out d-flex flex-justify-between flex-items-center flex-auto">
      <div class="d-none">
        <button class="btn-link js-details-target" type="button" aria-label="Toggle navigation" aria-expanded="false">
          <svg height="24" class="octicon octicon-x text-gray" viewBox="0 0 12 16" version="1.1" width="18" aria-hidden="true"><path fill-rule="evenodd" d="M7.48 8l3.75 3.75-1.48 1.48L6 9.48l-3.75 3.75-1.48-1.48L4.52 8 .77 4.25l1.48-1.48L6 6.52l3.75-3.75 1.48 1.48L7.48 8z"/></svg>
        </button>
      </div>

        <nav class="mt-0" aria-label="Global">
          <ul class="d-flex list-style-none">
              <li class=" mr-3 mr-lg-3 edge-item-fix position-relative flex-wrap flex-justify-between d-flex flex-items-center ">
                <details class="HeaderMenu-details details-overlay details-reset width-full">
                  <summary class="HeaderMenu-summary HeaderMenu-link px-0 py-3 border-0 no-wrap  d-inline-block">
                    Why GitHub?
                    <svg x="0px" y="0px" viewBox="0 0 14 8" xml:space="preserve" fill="none" class="icon-chevon-down-mktg position-relative">
                      <path d="M1,1l6.2,6L13,1"></path>
                    </svg>
                  </summary>
                  <div class="dropdown-menu flex-auto rounded-1 bg-white px-0 mt-0  p-4 left-n4 position-absolute">
                    <a href="/features" class="py-2 lh-condensed-ultra d-block link-gray-dark no-underline h5 Bump-link--hover" data-ga-click="(Logged out) Header, go to Features">Features <span class="Bump-link-symbol float-right text-normal text-gray-light">&rarr;</span></a>
                    <ul class="list-style-none f5 pb-3">
                      <li class="edge-item-fix"><a href="/features/code-review/" class="py-2 lh-condensed-ultra d-block link-gray no-underline f5" data-ga-click="(Logged out) Header, go to Code review">Code review</a></li>
                      <li class="edge-item-fix"><a href="/features/project-management/" class="py-2 lh-condensed-ultra d-block link-gray no-underline f5" data-ga-click="(Logged out) Header, go to Project management">Project management</a></li>
                      <li class="edge-item-fix"><a href="/features/integrations" class="py-2 lh-condensed-ultra d-block link-gray no-underline f5" data-ga-click="(Logged out) Header, go to Integrations">Integrations</a></li>
                      <li class="edge-item-fix"><a href="/features/actions" class="py-2 lh-condensed-ultra d-block link-gray no-underline f5" data-ga-click="(Logged out) Header, go to Actions">Actions</a>
                      <li class="edge-item-fix"><a href="/features#team-management" class="py-2 lh-condensed-ultra d-block link-gray no-underline f5" data-ga-click="(Logged out) Header, go to Team management">Team management</a></li>
                      <li class="edge-item-fix"><a href="/features#social-coding" class="py-2 lh-condensed-ultra d-block link-gray no-underline f5" data-ga-click="(Logged out) Header, go to Social coding">Social coding</a></li>
                      <li class="edge-item-fix"><a href="/features#documentation" class="py-2 lh-condensed-ultra d-block link-gray no-underline f5" data-ga-click="(Logged out) Header, go to Documentation">Documentation</a></li>
                      <li class="edge-item-fix"><a href="/features#code-hosting" class="py-2 lh-condensed-ultra d-block link-gray no-underline f5" data-ga-click="(Logged out) Header, go to Code hosting">Code hosting</a></li>
                    </ul>

                    <ul class="list-style-none mb-0 border-lg-top pt-lg-3">
                      <li class="edge-item-fix"><a href="/customer-stories" class="py-2 lh-condensed-ultra d-block no-underline link-gray-dark no-underline h5 Bump-link--hover" data-ga-click="(Logged out) Header, go to Customer stories">Customer stories <span class="Bump-link-symbol float-right text-normal text-gray-light">&rarr;</span></a></li>
                      <li class="edge-item-fix"><a href="/security" class="py-2 lh-condensed-ultra d-block no-underline link-gray-dark no-underline h5 Bump-link--hover" data-ga-click="(Logged out) Header, go to Security">Security <span class="Bump-link-symbol float-right text-normal text-gray-light">&rarr;</span></a></li>
                    </ul>
                  </div>
                </details>
              </li>
              <li class=" mr-3 mr-lg-3">
                <a href="/enterprise" class="HeaderMenu-link no-underline py-3 d-block d-lg-inline-block" data-ga-click="(Logged out) Header, go to Enterprise">Enterprise</a>
              </li>

              <li class=" mr-3 mr-lg-3 edge-item-fix position-relative flex-wrap flex-justify-between d-flex flex-items-center ">
                <details class="HeaderMenu-details details-overlay details-reset width-full">
                  <summary class="HeaderMenu-summary HeaderMenu-link px-0 py-3 border-0 no-wrap  d-inline-block">
                    Explore
                    <svg x="0px" y="0px" viewBox="0 0 14 8" xml:space="preserve" fill="none" class="icon-chevon-down-mktg position-relative">
                      <path d="M1,1l6.2,6L13,1"></path>
                    </svg>
                  </summary>

                  <div class="dropdown-menu flex-auto rounded-1 bg-white px-0 pt-2 pb-0 mt-0  p-4 left-n4 position-absolute">
                    <ul class="list-style-none mb-3">
                      <li class="edge-item-fix"><a href="/explore" class="py-2 lh-condensed-ultra d-block link-gray-dark no-underline h5 Bump-link--hover" data-ga-click="(Logged out) Header, go to Explore">Explore GitHub <span class="Bump-link-symbol float-right text-normal text-gray-light">&rarr;</span></a></li>
                    </ul>

                    <h4 class="text-gray-light text-normal text-mono f5 mb-2  border-top pt-3">Learn &amp; contribute</h4>
                    <ul class="list-style-none mb-3">
                      <li class="edge-item-fix"><a href="/topics" class="py-2 lh-condensed-ultra d-block link-gray no-underline f5" data-ga-click="(Logged out) Header, go to Topics">Topics</a></li>
                        <li class="edge-item-fix"><a href="/collections" class="py-2 lh-condensed-ultra d-block link-gray no-underline f5" data-ga-click="(Logged out) Header, go to Collections">Collections</a></li>
                      <li class="edge-item-fix"><a href="/trending" class="py-2 lh-condensed-ultra d-block link-gray no-underline f5" data-ga-click="(Logged out) Header, go to Trending">Trending</a></li>
                      <li class="edge-item-fix"><a href="https://lab.github.com/" class="py-2 lh-condensed-ultra d-block link-gray no-underline f5" data-ga-click="(Logged out) Header, go to Learning lab">Learning Lab</a></li>
                      <li class="edge-item-fix"><a href="https://opensource.guide" class="py-2 lh-condensed-ultra d-block link-gray no-underline f5" data-ga-click="(Logged out) Header, go to Open source guides">Open source guides</a></li>
                    </ul>

                    <h4 class="text-gray-light text-normal text-mono f5 mb-2  border-top pt-3">Connect with others</h4>
                    <ul class="list-style-none mb-0">
                      <li class="edge-item-fix"><a href="https://github.com/events" class="py-2 lh-condensed-ultra d-block link-gray no-underline f5" data-ga-click="(Logged out) Header, go to Events">Events</a></li>
                      <li class="edge-item-fix"><a href="https://github.community" class="py-2 lh-condensed-ultra d-block link-gray no-underline f5" data-ga-click="(Logged out) Header, go to Community forum">Community forum</a></li>
                      <li class="edge-item-fix"><a href="https://education.github.com" class="py-2 pb-0 lh-condensed-ultra d-block link-gray no-underline f5" data-ga-click="(Logged out) Header, go to GitHub Education">GitHub Education</a></li>
                    </ul>
                  </div>
                </details>
              </li>

              <li class=" mr-3 mr-lg-3">
                <a href="/marketplace" class="HeaderMenu-link no-underline py-3 d-block d-lg-inline-block" data-ga-click="(Logged out) Header, go to Marketplace">Marketplace</a>
              </li>

              <li class=" mr-3 mr-lg-3 edge-item-fix position-relative flex-wrap flex-justify-between d-flex flex-items-center ">
                <details class="HeaderMenu-details details-overlay details-reset width-full">
                  <summary class="HeaderMenu-summary HeaderMenu-link px-0 py-3 border-0 no-wrap  d-inline-block">
                    Pricing
                    <svg x="0px" y="0px" viewBox="0 0 14 8" xml:space="preserve" fill="none" class="icon-chevon-down-mktg position-relative">
                       <path d="M1,1l6.2,6L13,1"></path>
                    </svg>
                  </summary>

                  <div class="dropdown-menu flex-auto rounded-1 bg-white px-0 pt-2 pb-4 mt-0  p-4 left-n4 position-absolute">
                    <a href="/pricing" class="pb-2 lh-condensed-ultra d-block link-gray-dark no-underline h5 Bump-link--hover" data-ga-click="(Logged out) Header, go to Pricing">Plans <span class="Bump-link-symbol float-right text-normal text-gray-light">&rarr;</span></a>

                    <ul class="list-style-none mb-3">
                      <li class="edge-item-fix"><a href="/pricing#feature-comparison" class="py-2 lh-condensed-ultra d-block link-gray no-underline f5" data-ga-click="(Logged out) Header, go to Compare plans">Compare plans</a></li>
                      <li class="edge-item-fix"><a href="https://enterprise.github.com/contact" class="py-2 lh-condensed-ultra d-block link-gray no-underline f5" data-ga-click="(Logged out) Header, go to Contact Sales">Contact Sales</a></li>
                    </ul>

                    <ul class="list-style-none mb-0  border-top pt-3">
                      <li class="edge-item-fix"><a href="/nonprofit" class="py-2 lh-condensed-ultra d-block no-underline link-gray-dark no-underline h5 Bump-link--hover" data-ga-click="(Logged out) Header, go to Nonprofits">Nonprofit <span class="Bump-link-symbol float-right text-normal text-gray-light">&rarr;</span></a></li>
                      <li class="edge-item-fix"><a href="https://education.github.com" class="py-2 pb-0 lh-condensed-ultra d-block no-underline link-gray-dark no-underline h5 Bump-link--hover"  data-ga-click="(Logged out) Header, go to Education">Education <span class="Bump-link-symbol float-right text-normal text-gray-light">&rarr;</span></a></li>
                    </ul>
                  </div>
                </details>
              </li>
          </ul>
        </nav>

      <div class="d-flex flex-items-center px-0 text-center text-left">
          <div class="d-lg-flex ">
            <div class="header-search mr-3 scoped-search site-scoped-search js-site-search position-relative js-jump-to"
  role="combobox"
  aria-owns="jump-to-results"
  aria-label="Search or jump to"
  aria-haspopup="listbox"
  aria-expanded="false"
>
  <div class="position-relative">
    <!-- '"` --><!-- </textarea></xmp> --></option></form><form class="js-site-search-form" role="search" aria-label="Site" data-scope-type="Repository" data-scope-id="64188788" data-scoped-search-url="/pingcap/docs-cn/search" data-unscoped-search-url="/search" action="/pingcap/docs-cn/search" accept-charset="UTF-8" method="get"><input name="utf8" type="hidden" value="&#x2713;" />
      <label class="form-control input-sm header-search-wrapper p-0 header-search-wrapper-jump-to position-relative d-flex flex-justify-between flex-items-center js-chromeless-input-container">
        <input type="text"
          class="form-control input-sm header-search-input jump-to-field js-jump-to-field js-site-search-focus js-site-search-field is-clearable"
          data-hotkey="s,/"
          name="q"
          value=""
          placeholder="Search"
          data-unscoped-placeholder="Search GitHub"
          data-scoped-placeholder="Search"
          autocapitalize="off"
          aria-autocomplete="list"
          aria-controls="jump-to-results"
          aria-label="Search"
          data-jump-to-suggestions-path="/_graphql/GetSuggestedNavigationDestinations#csrf-token=E5oYgd6BowxZJg5afciKEtoSd/f0eZcVEJVl+bUAQrjLaZU4t7MHCkTT7CA+mGg1tEoukf2uVi/aunDTrbCsfQ=="
          spellcheck="false"
          autocomplete="off"
          >
          <input type="hidden" class="js-site-search-type-field" name="type" >
            <img src="https://github.githubassets.com/images/search-key-slash.svg" alt="" class="mr-2 header-search-key-slash">

            <div class="Box position-absolute overflow-hidden d-none jump-to-suggestions js-jump-to-suggestions-container">
              
<ul class="d-none js-jump-to-suggestions-template-container">
  

<li class="d-flex flex-justify-start flex-items-center p-0 f5 navigation-item js-navigation-item js-jump-to-suggestion" role="option">
  <a tabindex="-1" class="no-underline d-flex flex-auto flex-items-center jump-to-suggestions-path js-jump-to-suggestion-path js-navigation-open p-2" href="">
    <div class="jump-to-octicon js-jump-to-octicon flex-shrink-0 mr-2 text-center d-none">
      <svg height="16" width="16" class="octicon octicon-repo flex-shrink-0 js-jump-to-octicon-repo d-none" title="Repository" aria-label="Repository" viewBox="0 0 12 16" version="1.1" role="img"><path fill-rule="evenodd" d="M4 9H3V8h1v1zm0-3H3v1h1V6zm0-2H3v1h1V4zm0-2H3v1h1V2zm8-1v12c0 .55-.45 1-1 1H6v2l-1.5-1.5L3 16v-2H1c-.55 0-1-.45-1-1V1c0-.55.45-1 1-1h10c.55 0 1 .45 1 1zm-1 10H1v2h2v-1h3v1h5v-2zm0-10H2v9h9V1z"/></svg>
      <svg height="16" width="16" class="octicon octicon-project flex-shrink-0 js-jump-to-octicon-project d-none" title="Project" aria-label="Project" viewBox="0 0 15 16" version="1.1" role="img"><path fill-rule="evenodd" d="M10 12h3V2h-3v10zm-4-2h3V2H6v8zm-4 4h3V2H2v12zm-1 1h13V1H1v14zM14 0H1a1 1 0 0 0-1 1v14a1 1 0 0 0 1 1h13a1 1 0 0 0 1-1V1a1 1 0 0 0-1-1z"/></svg>
      <svg height="16" width="16" class="octicon octicon-search flex-shrink-0 js-jump-to-octicon-search d-none" title="Search" aria-label="Search" viewBox="0 0 16 16" version="1.1" role="img"><path fill-rule="evenodd" d="M15.7 13.3l-3.81-3.83A5.93 5.93 0 0 0 13 6c0-3.31-2.69-6-6-6S1 2.69 1 6s2.69 6 6 6c1.3 0 2.48-.41 3.47-1.11l3.83 3.81c.19.2.45.3.7.3.25 0 .52-.09.7-.3a.996.996 0 0 0 0-1.41v.01zM7 10.7c-2.59 0-4.7-2.11-4.7-4.7 0-2.59 2.11-4.7 4.7-4.7 2.59 0 4.7 2.11 4.7 4.7 0 2.59-2.11 4.7-4.7 4.7z"/></svg>
    </div>

    <img class="avatar mr-2 flex-shrink-0 js-jump-to-suggestion-avatar d-none" alt="" aria-label="Team" src="" width="28" height="28">

    <div class="jump-to-suggestion-name js-jump-to-suggestion-name flex-auto overflow-hidden text-left no-wrap css-truncate css-truncate-target">
    </div>

    <div class="border rounded-1 flex-shrink-0 bg-gray px-1 text-gray-light ml-1 f6 d-none js-jump-to-badge-search">
      <span class="js-jump-to-badge-search-text-default d-none" aria-label="in this repository">
        In this repository
      </span>
      <span class="js-jump-to-badge-search-text-global d-none" aria-label="in all of GitHub">
        All GitHub
      </span>
      <span aria-hidden="true" class="d-inline-block ml-1 v-align-middle">↵</span>
    </div>

    <div aria-hidden="true" class="border rounded-1 flex-shrink-0 bg-gray px-1 text-gray-light ml-1 f6 d-none d-on-nav-focus js-jump-to-badge-jump">
      Jump to
      <span class="d-inline-block ml-1 v-align-middle">↵</span>
    </div>
  </a>
</li>

</ul>

<ul class="d-none js-jump-to-no-results-template-container">
  <li class="d-flex flex-justify-center flex-items-center f5 d-none js-jump-to-suggestion p-2">
    <span class="text-gray">No suggested jump to results</span>
  </li>
</ul>

<ul id="jump-to-results" role="listbox" class="p-0 m-0 js-navigation-container jump-to-suggestions-results-container js-jump-to-suggestions-results-container">
  

<li class="d-flex flex-justify-start flex-items-center p-0 f5 navigation-item js-navigation-item js-jump-to-scoped-search d-none" role="option">
  <a tabindex="-1" class="no-underline d-flex flex-auto flex-items-center jump-to-suggestions-path js-jump-to-suggestion-path js-navigation-open p-2" href="">
    <div class="jump-to-octicon js-jump-to-octicon flex-shrink-0 mr-2 text-center d-none">
      <svg height="16" width="16" class="octicon octicon-repo flex-shrink-0 js-jump-to-octicon-repo d-none" title="Repository" aria-label="Repository" viewBox="0 0 12 16" version="1.1" role="img"><path fill-rule="evenodd" d="M4 9H3V8h1v1zm0-3H3v1h1V6zm0-2H3v1h1V4zm0-2H3v1h1V2zm8-1v12c0 .55-.45 1-1 1H6v2l-1.5-1.5L3 16v-2H1c-.55 0-1-.45-1-1V1c0-.55.45-1 1-1h10c.55 0 1 .45 1 1zm-1 10H1v2h2v-1h3v1h5v-2zm0-10H2v9h9V1z"/></svg>
      <svg height="16" width="16" class="octicon octicon-project flex-shrink-0 js-jump-to-octicon-project d-none" title="Project" aria-label="Project" viewBox="0 0 15 16" version="1.1" role="img"><path fill-rule="evenodd" d="M10 12h3V2h-3v10zm-4-2h3V2H6v8zm-4 4h3V2H2v12zm-1 1h13V1H1v14zM14 0H1a1 1 0 0 0-1 1v14a1 1 0 0 0 1 1h13a1 1 0 0 0 1-1V1a1 1 0 0 0-1-1z"/></svg>
      <svg height="16" width="16" class="octicon octicon-search flex-shrink-0 js-jump-to-octicon-search d-none" title="Search" aria-label="Search" viewBox="0 0 16 16" version="1.1" role="img"><path fill-rule="evenodd" d="M15.7 13.3l-3.81-3.83A5.93 5.93 0 0 0 13 6c0-3.31-2.69-6-6-6S1 2.69 1 6s2.69 6 6 6c1.3 0 2.48-.41 3.47-1.11l3.83 3.81c.19.2.45.3.7.3.25 0 .52-.09.7-.3a.996.996 0 0 0 0-1.41v.01zM7 10.7c-2.59 0-4.7-2.11-4.7-4.7 0-2.59 2.11-4.7 4.7-4.7 2.59 0 4.7 2.11 4.7 4.7 0 2.59-2.11 4.7-4.7 4.7z"/></svg>
    </div>

    <img class="avatar mr-2 flex-shrink-0 js-jump-to-suggestion-avatar d-none" alt="" aria-label="Team" src="" width="28" height="28">

    <div class="jump-to-suggestion-name js-jump-to-suggestion-name flex-auto overflow-hidden text-left no-wrap css-truncate css-truncate-target">
    </div>

    <div class="border rounded-1 flex-shrink-0 bg-gray px-1 text-gray-light ml-1 f6 d-none js-jump-to-badge-search">
      <span class="js-jump-to-badge-search-text-default d-none" aria-label="in this repository">
        In this repository
      </span>
      <span class="js-jump-to-badge-search-text-global d-none" aria-label="in all of GitHub">
        All GitHub
      </span>
      <span aria-hidden="true" class="d-inline-block ml-1 v-align-middle">↵</span>
    </div>

    <div aria-hidden="true" class="border rounded-1 flex-shrink-0 bg-gray px-1 text-gray-light ml-1 f6 d-none d-on-nav-focus js-jump-to-badge-jump">
      Jump to
      <span class="d-inline-block ml-1 v-align-middle">↵</span>
    </div>
  </a>
</li>

  

<li class="d-flex flex-justify-start flex-items-center p-0 f5 navigation-item js-navigation-item js-jump-to-global-search d-none" role="option">
  <a tabindex="-1" class="no-underline d-flex flex-auto flex-items-center jump-to-suggestions-path js-jump-to-suggestion-path js-navigation-open p-2" href="">
    <div class="jump-to-octicon js-jump-to-octicon flex-shrink-0 mr-2 text-center d-none">
      <svg height="16" width="16" class="octicon octicon-repo flex-shrink-0 js-jump-to-octicon-repo d-none" title="Repository" aria-label="Repository" viewBox="0 0 12 16" version="1.1" role="img"><path fill-rule="evenodd" d="M4 9H3V8h1v1zm0-3H3v1h1V6zm0-2H3v1h1V4zm0-2H3v1h1V2zm8-1v12c0 .55-.45 1-1 1H6v2l-1.5-1.5L3 16v-2H1c-.55 0-1-.45-1-1V1c0-.55.45-1 1-1h10c.55 0 1 .45 1 1zm-1 10H1v2h2v-1h3v1h5v-2zm0-10H2v9h9V1z"/></svg>
      <svg height="16" width="16" class="octicon octicon-project flex-shrink-0 js-jump-to-octicon-project d-none" title="Project" aria-label="Project" viewBox="0 0 15 16" version="1.1" role="img"><path fill-rule="evenodd" d="M10 12h3V2h-3v10zm-4-2h3V2H6v8zm-4 4h3V2H2v12zm-1 1h13V1H1v14zM14 0H1a1 1 0 0 0-1 1v14a1 1 0 0 0 1 1h13a1 1 0 0 0 1-1V1a1 1 0 0 0-1-1z"/></svg>
      <svg height="16" width="16" class="octicon octicon-search flex-shrink-0 js-jump-to-octicon-search d-none" title="Search" aria-label="Search" viewBox="0 0 16 16" version="1.1" role="img"><path fill-rule="evenodd" d="M15.7 13.3l-3.81-3.83A5.93 5.93 0 0 0 13 6c0-3.31-2.69-6-6-6S1 2.69 1 6s2.69 6 6 6c1.3 0 2.48-.41 3.47-1.11l3.83 3.81c.19.2.45.3.7.3.25 0 .52-.09.7-.3a.996.996 0 0 0 0-1.41v.01zM7 10.7c-2.59 0-4.7-2.11-4.7-4.7 0-2.59 2.11-4.7 4.7-4.7 2.59 0 4.7 2.11 4.7 4.7 0 2.59-2.11 4.7-4.7 4.7z"/></svg>
    </div>

    <img class="avatar mr-2 flex-shrink-0 js-jump-to-suggestion-avatar d-none" alt="" aria-label="Team" src="" width="28" height="28">

    <div class="jump-to-suggestion-name js-jump-to-suggestion-name flex-auto overflow-hidden text-left no-wrap css-truncate css-truncate-target">
    </div>

    <div class="border rounded-1 flex-shrink-0 bg-gray px-1 text-gray-light ml-1 f6 d-none js-jump-to-badge-search">
      <span class="js-jump-to-badge-search-text-default d-none" aria-label="in this repository">
        In this repository
      </span>
      <span class="js-jump-to-badge-search-text-global d-none" aria-label="in all of GitHub">
        All GitHub
      </span>
      <span aria-hidden="true" class="d-inline-block ml-1 v-align-middle">↵</span>
    </div>

    <div aria-hidden="true" class="border rounded-1 flex-shrink-0 bg-gray px-1 text-gray-light ml-1 f6 d-none d-on-nav-focus js-jump-to-badge-jump">
      Jump to
      <span class="d-inline-block ml-1 v-align-middle">↵</span>
    </div>
  </a>
</li>


</ul>

            </div>
      </label>
</form>  </div>
</div>

          </div>

        <a class="HeaderMenu-link no-underline mr-3" data-hydro-click="{&quot;event_type&quot;:&quot;authentication.click&quot;,&quot;payload&quot;:{&quot;location_in_page&quot;:&quot;site header menu&quot;,&quot;repository_id&quot;:null,&quot;auth_type&quot;:&quot;LOG_IN&quot;,&quot;client_id&quot;:null,&quot;originating_request_id&quot;:&quot;3BFF:4B8D:CFCFF:12D50B:5CC010B0&quot;,&quot;originating_url&quot;:&quot;https://github.com/pingcap/docs-cn/blob/master/benchmark/sysbench.md&quot;,&quot;referrer&quot;:null,&quot;user_id&quot;:null}}" data-hydro-click-hmac="0183be3c4749c1f70ab6a1bad4b519d7abe2830aa7a5ed11bba811cda62fd773" data-ga-click="(Logged out) Header, clicked Sign in, text:sign-in" href="/login?return_to=%2Fpingcap%2Fdocs-cn%2Fblob%2Fmaster%2Fbenchmark%2Fsysbench.md">
          Sign&nbsp;in
</a>          <a class="HeaderMenu-link d-inline-block no-underline border border-gray-dark rounded-1 px-2 py-1" data-hydro-click="{&quot;event_type&quot;:&quot;authentication.click&quot;,&quot;payload&quot;:{&quot;location_in_page&quot;:&quot;site header menu&quot;,&quot;repository_id&quot;:null,&quot;auth_type&quot;:&quot;SIGN_UP&quot;,&quot;client_id&quot;:null,&quot;originating_request_id&quot;:&quot;3BFF:4B8D:CFCFF:12D50B:5CC010B0&quot;,&quot;originating_url&quot;:&quot;https://github.com/pingcap/docs-cn/blob/master/benchmark/sysbench.md&quot;,&quot;referrer&quot;:null,&quot;user_id&quot;:null}}" data-hydro-click-hmac="06e8f16a78bac778297e2f3702cc992f46b4b457f5b0de3b66e8e716f022c507" data-ga-click="(Logged out) Header, clicked Sign up, text:sign-up" href="/join">
            Sign&nbsp;up
</a>      </div>
    </div>
  </div>
</header>

  </div>

  <div id="start-of-content" class="show-on-focus"></div>


    <div id="js-flash-container">

</div>



  <div class="application-main " data-commit-hovercards-enabled>
        <div itemscope itemtype="http://schema.org/SoftwareSourceCode" class="">
    <main id="js-repo-pjax-container" data-pjax-container >
      


  



  




  <div class="pagehead repohead instapaper_ignore readability-menu experiment-repo-nav  ">
    <div class="repohead-details-container clearfix container">

      <ul class="pagehead-actions">



  <li>
    
  <a class="tooltipped tooltipped-s btn btn-sm btn-with-count" aria-label="You must be signed in to watch a repository" rel="nofollow" data-hydro-click="{&quot;event_type&quot;:&quot;authentication.click&quot;,&quot;payload&quot;:{&quot;location_in_page&quot;:&quot;notification subscription menu watch&quot;,&quot;repository_id&quot;:null,&quot;auth_type&quot;:&quot;LOG_IN&quot;,&quot;client_id&quot;:null,&quot;originating_request_id&quot;:&quot;3BFF:4B8D:CFCFF:12D50B:5CC010B0&quot;,&quot;originating_url&quot;:&quot;https://github.com/pingcap/docs-cn/blob/master/benchmark/sysbench.md&quot;,&quot;referrer&quot;:null,&quot;user_id&quot;:null}}" data-hydro-click-hmac="549d4dfcd161782fae86d92831c3a6dbfd190b590e7aceb2d77947977380336f" href="/login?return_to=%2Fpingcap%2Fdocs-cn">
    <svg class="octicon octicon-eye v-align-text-bottom" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M8.06 2C3 2 0 8 0 8s3 6 8.06 6C13 14 16 8 16 8s-3-6-7.94-6zM8 12c-2.2 0-4-1.78-4-4 0-2.2 1.8-4 4-4 2.22 0 4 1.8 4 4 0 2.22-1.78 4-4 4zm2-4c0 1.11-.89 2-2 2-1.11 0-2-.89-2-2 0-1.11.89-2 2-2 1.11 0 2 .89 2 2z"/></svg>
    Watch
</a>    <a class="social-count" href="/pingcap/docs-cn/watchers"
       aria-label="173 users are watching this repository">
      173
    </a>

  </li>

  <li>
        <a class="btn btn-sm btn-with-count tooltipped tooltipped-s" aria-label="You must be signed in to star a repository" rel="nofollow" data-hydro-click="{&quot;event_type&quot;:&quot;authentication.click&quot;,&quot;payload&quot;:{&quot;location_in_page&quot;:&quot;star button&quot;,&quot;repository_id&quot;:64188788,&quot;auth_type&quot;:&quot;LOG_IN&quot;,&quot;client_id&quot;:null,&quot;originating_request_id&quot;:&quot;3BFF:4B8D:CFCFF:12D50B:5CC010B0&quot;,&quot;originating_url&quot;:&quot;https://github.com/pingcap/docs-cn/blob/master/benchmark/sysbench.md&quot;,&quot;referrer&quot;:null,&quot;user_id&quot;:null}}" data-hydro-click-hmac="1add1d9a9f83756315d37a7de0ea7109fae7990c869c243ffb44931d30d63c39" href="/login?return_to=%2Fpingcap%2Fdocs-cn">
      <svg class="octicon octicon-star v-align-text-bottom" viewBox="0 0 14 16" version="1.1" width="14" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M14 6l-4.9-.64L7 1 4.9 5.36 0 6l3.6 3.26L2.67 14 7 11.67 11.33 14l-.93-4.74L14 6z"/></svg>
      Star
</a>
    <a class="social-count js-social-count" href="/pingcap/docs-cn/stargazers"
      aria-label="1238 users starred this repository">
      1,238
    </a>

  </li>

  <li>
      <a class="btn btn-sm btn-with-count tooltipped tooltipped-s" aria-label="You must be signed in to fork a repository" rel="nofollow" data-hydro-click="{&quot;event_type&quot;:&quot;authentication.click&quot;,&quot;payload&quot;:{&quot;location_in_page&quot;:&quot;repo details fork button&quot;,&quot;repository_id&quot;:64188788,&quot;auth_type&quot;:&quot;LOG_IN&quot;,&quot;client_id&quot;:null,&quot;originating_request_id&quot;:&quot;3BFF:4B8D:CFCFF:12D50B:5CC010B0&quot;,&quot;originating_url&quot;:&quot;https://github.com/pingcap/docs-cn/blob/master/benchmark/sysbench.md&quot;,&quot;referrer&quot;:null,&quot;user_id&quot;:null}}" data-hydro-click-hmac="11fddf9792dbd26c0998373bb4df3c98b012bd81cdaaeae41490f9d0264ecac8" href="/login?return_to=%2Fpingcap%2Fdocs-cn">
        <svg class="octicon octicon-repo-forked v-align-text-bottom" viewBox="0 0 10 16" version="1.1" width="10" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M8 1a1.993 1.993 0 0 0-1 3.72V6L5 8 3 6V4.72A1.993 1.993 0 0 0 2 1a1.993 1.993 0 0 0-1 3.72V6.5l3 3v1.78A1.993 1.993 0 0 0 5 15a1.993 1.993 0 0 0 1-3.72V9.5l3-3V4.72A1.993 1.993 0 0 0 8 1zM2 4.2C1.34 4.2.8 3.65.8 3c0-.65.55-1.2 1.2-1.2.65 0 1.2.55 1.2 1.2 0 .65-.55 1.2-1.2 1.2zm3 10c-.66 0-1.2-.55-1.2-1.2 0-.65.55-1.2 1.2-1.2.65 0 1.2.55 1.2 1.2 0 .65-.55 1.2-1.2 1.2zm3-10c-.66 0-1.2-.55-1.2-1.2 0-.65.55-1.2 1.2-1.2.65 0 1.2.55 1.2 1.2 0 .65-.55 1.2-1.2 1.2z"/></svg>
        Fork
</a>
    <a href="/pingcap/docs-cn/network/members" class="social-count"
       aria-label="456 users forked this repository">
      456
    </a>
  </li>
</ul>

      <h1 class="public ">
  <svg class="octicon octicon-repo" viewBox="0 0 12 16" version="1.1" width="12" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9H3V8h1v1zm0-3H3v1h1V6zm0-2H3v1h1V4zm0-2H3v1h1V2zm8-1v12c0 .55-.45 1-1 1H6v2l-1.5-1.5L3 16v-2H1c-.55 0-1-.45-1-1V1c0-.55.45-1 1-1h10c.55 0 1 .45 1 1zm-1 10H1v2h2v-1h3v1h5v-2zm0-10H2v9h9V1z"/></svg>
  <span class="author" itemprop="author"><a class="url fn" rel="author" data-hovercard-type="organization" data-hovercard-url="/orgs/pingcap/hovercard" href="/pingcap">pingcap</a></span><!--
--><span class="path-divider">/</span><!--
--><strong itemprop="name"><a data-pjax="#js-repo-pjax-container" href="/pingcap/docs-cn">docs-cn</a></strong>
  

</h1>

    </div>
    
<nav class="reponav js-repo-nav js-sidenav-container-pjax container"
     itemscope
     itemtype="http://schema.org/BreadcrumbList"
    aria-label="Repository"
     data-pjax="#js-repo-pjax-container">

  <span itemscope itemtype="http://schema.org/ListItem" itemprop="itemListElement">
    <a class="js-selected-navigation-item selected reponav-item" itemprop="url" data-hotkey="g c" aria-current="page" data-selected-links="repo_source repo_downloads repo_commits repo_releases repo_tags repo_branches repo_packages /pingcap/docs-cn" href="/pingcap/docs-cn">
      <svg class="octicon octicon-code" viewBox="0 0 14 16" version="1.1" width="14" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M9.5 3L8 4.5 11.5 8 8 11.5 9.5 13 14 8 9.5 3zm-5 0L0 8l4.5 5L6 11.5 2.5 8 6 4.5 4.5 3z"/></svg>
      <span itemprop="name">Code</span>
      <meta itemprop="position" content="1">
</a>  </span>

    <span itemscope itemtype="http://schema.org/ListItem" itemprop="itemListElement">
      <a itemprop="url" data-hotkey="g i" class="js-selected-navigation-item reponav-item" data-selected-links="repo_issues repo_labels repo_milestones /pingcap/docs-cn/issues" href="/pingcap/docs-cn/issues">
        <svg class="octicon octicon-issue-opened" viewBox="0 0 14 16" version="1.1" width="14" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7 2.3c3.14 0 5.7 2.56 5.7 5.7s-2.56 5.7-5.7 5.7A5.71 5.71 0 0 1 1.3 8c0-3.14 2.56-5.7 5.7-5.7zM7 1C3.14 1 0 4.14 0 8s3.14 7 7 7 7-3.14 7-7-3.14-7-7-7zm1 3H6v5h2V4zm0 6H6v2h2v-2z"/></svg>
        <span itemprop="name">Issues</span>
        <span class="Counter">51</span>
        <meta itemprop="position" content="2">
</a>    </span>

  <span itemscope itemtype="http://schema.org/ListItem" itemprop="itemListElement">
    <a data-hotkey="g p" itemprop="url" class="js-selected-navigation-item reponav-item" data-selected-links="repo_pulls checks /pingcap/docs-cn/pulls" href="/pingcap/docs-cn/pulls">
      <svg class="octicon octicon-git-pull-request" viewBox="0 0 12 16" version="1.1" width="12" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M11 11.28V5c-.03-.78-.34-1.47-.94-2.06C9.46 2.35 8.78 2.03 8 2H7V0L4 3l3 3V4h1c.27.02.48.11.69.31.21.2.3.42.31.69v6.28A1.993 1.993 0 0 0 10 15a1.993 1.993 0 0 0 1-3.72zm-1 2.92c-.66 0-1.2-.55-1.2-1.2 0-.65.55-1.2 1.2-1.2.65 0 1.2.55 1.2 1.2 0 .65-.55 1.2-1.2 1.2zM4 3c0-1.11-.89-2-2-2a1.993 1.993 0 0 0-1 3.72v6.56A1.993 1.993 0 0 0 2 15a1.993 1.993 0 0 0 1-3.72V4.72c.59-.34 1-.98 1-1.72zm-.8 10c0 .66-.55 1.2-1.2 1.2-.65 0-1.2-.55-1.2-1.2 0-.65.55-1.2 1.2-1.2.65 0 1.2.55 1.2 1.2zM2 4.2C1.34 4.2.8 3.65.8 3c0-.65.55-1.2 1.2-1.2.65 0 1.2.55 1.2 1.2 0 .65-.55 1.2-1.2 1.2z"/></svg>
      <span itemprop="name">Pull requests</span>
      <span class="Counter">11</span>
      <meta itemprop="position" content="3">
</a>  </span>



    <a data-hotkey="g b" class="js-selected-navigation-item reponav-item" data-selected-links="repo_projects new_repo_project repo_project /pingcap/docs-cn/projects" href="/pingcap/docs-cn/projects">
      <svg class="octicon octicon-project" viewBox="0 0 15 16" version="1.1" width="15" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M10 12h3V2h-3v10zm-4-2h3V2H6v8zm-4 4h3V2H2v12zm-1 1h13V1H1v14zM14 0H1a1 1 0 0 0-1 1v14a1 1 0 0 0 1 1h13a1 1 0 0 0 1-1V1a1 1 0 0 0-1-1z"/></svg>
      Projects
      <span class="Counter" >0</span>
</a>


    <a class="js-selected-navigation-item reponav-item" data-selected-links="repo_graphs repo_contributors dependency_graph pulse people alerts /pingcap/docs-cn/pulse" href="/pingcap/docs-cn/pulse">
      <svg class="octicon octicon-graph" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M16 14v1H0V0h1v14h15zM5 13H3V8h2v5zm4 0H7V3h2v10zm4 0h-2V6h2v7z"/></svg>
      Insights
</a>

</nav>


  </div>
<div class="container new-discussion-timeline experiment-repo-nav  ">
  <div class="repository-content ">

    
    



  
    <a class="d-none js-permalink-shortcut" data-hotkey="y" href="/pingcap/docs-cn/blob/9744a56fcb25ecaae05dc9175dacd4901b2215a3/benchmark/sysbench.md">Permalink</a>

    <!-- blob contrib key: blob_contributors:v21:06a79b9d8cedbbe914cd4623e2610a2e -->
          <div class="signup-prompt-bg rounded-1">
      <div class="signup-prompt p-4 text-center mb-4 rounded-1">
        <div class="position-relative">
          <!-- '"` --><!-- </textarea></xmp> --></option></form><form action="/prompt_dismissals/signup" accept-charset="UTF-8" method="post"><input name="utf8" type="hidden" value="&#x2713;" /><input type="hidden" name="_method" value="put" /><input type="hidden" name="authenticity_token" value="U67D5OR7F5IXOObDph9BdrlEF45Xnq7YwVKsDkg52/1/oiadV0dNk0Std5c0DiOZO58evSkp/esQ1f7ozbN1Pw==" />
            <button type="submit" class="position-absolute top-0 right-0 btn-link link-gray" data-ga-click="(Logged out) Sign up prompt, clicked Dismiss, text:dismiss">
              Dismiss
            </button>
</form>          <h3 class="pt-2">Join GitHub today</h3>
          <p class="col-6 mx-auto">GitHub is home to over 31 million developers working together to host and review code, manage projects, and build software together.</p>
          <a class="btn btn-primary" data-hydro-click="{&quot;event_type&quot;:&quot;authentication.click&quot;,&quot;payload&quot;:{&quot;location_in_page&quot;:&quot;files signup prompt&quot;,&quot;repository_id&quot;:null,&quot;auth_type&quot;:&quot;SIGN_UP&quot;,&quot;client_id&quot;:null,&quot;originating_request_id&quot;:&quot;3BFF:4B8D:CFCFF:12D50B:5CC010B0&quot;,&quot;originating_url&quot;:&quot;https://github.com/pingcap/docs-cn/blob/master/benchmark/sysbench.md&quot;,&quot;referrer&quot;:null,&quot;user_id&quot;:null}}" data-hydro-click-hmac="e2c4d5b5a72047b3706b8d8737f98c49edff26dbfe4ab876c494337b59c1df5c" data-ga-click="(Logged out) Sign up prompt, clicked Sign up, text:sign-up" href="/join?source=prompt-blob-show">Sign up</a>
        </div>
      </div>
    </div>


    <div class="d-flex flex-items-start mb-3">
      <span class="d-flex flex-justify-between">
        
<details class="details-reset details-overlay select-menu branch-select-menu ">
  <summary class="btn btn-sm select-menu-button css-truncate"
           data-hotkey="w"
           
           title="Switch branches or tags">
    <i>Branch:</i>
    <span class="css-truncate-target">master</span>
  </summary>

  <details-menu class="select-menu-modal position-absolute" style="z-index: 99;" src="/pingcap/docs-cn/ref-list/master/benchmark/sysbench.md?source_action=show&amp;source_controller=blob" preload>
    <include-fragment class="select-menu-loading-overlay anim-pulse">
      <svg height="32" class="octicon octicon-octoface" viewBox="0 0 16 16" version="1.1" width="32" aria-hidden="true"><path fill-rule="evenodd" d="M14.7 5.34c.13-.32.55-1.59-.13-3.31 0 0-1.05-.33-3.44 1.3-1-.28-2.07-.32-3.13-.32s-2.13.04-3.13.32c-2.39-1.64-3.44-1.3-3.44-1.3-.68 1.72-.26 2.99-.13 3.31C.49 6.21 0 7.33 0 8.69 0 13.84 3.33 15 7.98 15S16 13.84 16 8.69c0-1.36-.49-2.48-1.3-3.35zM8 14.02c-3.3 0-5.98-.15-5.98-3.35 0-.76.38-1.48 1.02-2.07 1.07-.98 2.9-.46 4.96-.46 2.07 0 3.88-.52 4.96.46.65.59 1.02 1.3 1.02 2.07 0 3.19-2.68 3.35-5.98 3.35zM5.49 9.01c-.66 0-1.2.8-1.2 1.78s.54 1.79 1.2 1.79c.66 0 1.2-.8 1.2-1.79s-.54-1.78-1.2-1.78zm5.02 0c-.66 0-1.2.79-1.2 1.78s.54 1.79 1.2 1.79c.66 0 1.2-.8 1.2-1.79s-.53-1.78-1.2-1.78z"/></svg>
    </include-fragment>
  </details-menu>
</details>

        <div class="BtnGroup flex-shrink-0 d-none">
          <a href="/pingcap/docs-cn/find/master"
                class="js-pjax-capture-input btn btn-sm BtnGroup-item"
                data-pjax
                data-hotkey="t">
            Find file
          </a>
          <clipboard-copy value="benchmark/sysbench.md" class="btn btn-sm BtnGroup-item">
            Copy path
          </clipboard-copy>
        </div>
      </span>
      <h2 id="blob-path" class="breadcrumb flex-auto min-width-0 text-normal ml-2 mr-3">
        <span class="js-repo-root text-bold"><span class="js-path-segment"><a data-pjax="true" href="/pingcap/docs-cn"><span>docs-cn</span></a></span></span><span class="separator">/</span><span class="js-path-segment"><a data-pjax="true" href="/pingcap/docs-cn/tree/master/benchmark"><span>benchmark</span></a></span><span class="separator">/</span><strong class="final-path">sysbench.md</strong>
      </h2>

      <div class="BtnGroup flex-shrink-0 d-inline-block">
        <a href="/pingcap/docs-cn/find/master"
              class="js-pjax-capture-input btn btn-sm BtnGroup-item"
              data-pjax
              data-hotkey="t">
          Find file
        </a>
        <clipboard-copy value="benchmark/sysbench.md" class="btn btn-sm BtnGroup-item">
          Copy path
        </clipboard-copy>
      </div>
    </div>



    
  <div class="Box Box--condensed d-flex flex-column flex-shrink-0">
      <div class="Box-body d-flex flex-justify-between bg-blue-light flex-column flex-md-row flex-items-start flex-md-items-center">
        <span class="pr-md-4 f6">
          <a rel="contributor" data-skip-pjax="true" data-hovercard-type="user" data-hovercard-url="/hovercards?user_id=34535727" data-octo-click="hovercard-link-click" data-octo-dimensions="link_type:self" href="/CaitinChen"><img class="avatar" src="https://avatars2.githubusercontent.com/u/34535727?s=40&amp;v=4" width="20" height="20" alt="@CaitinChen" /></a>
          <a class="text-bold link-gray-dark lh-default v-align-middle" rel="contributor" data-hovercard-type="user" data-hovercard-url="/hovercards?user_id=34535727" data-octo-click="hovercard-link-click" data-octo-dimensions="link_type:self" href="/CaitinChen">CaitinChen</a>
            <span class="lh-default v-align-middle">
              <a data-pjax="true" title="*: fix table format of 4 sysbench files" class="link-gray" href="/pingcap/docs-cn/commit/336164cd2bbd98a6e5f2a5e297e514cab6ec8d32">*: fix table format of 4 sysbench files</a>
            </span>
        </span>
        <span class="d-inline-block flex-shrink-0 v-align-bottom f6 mt-2 mt-md-0">
          <a class="pr-2 text-mono link-gray" href="/pingcap/docs-cn/commit/336164cd2bbd98a6e5f2a5e297e514cab6ec8d32" data-pjax>336164c</a>
          <relative-time datetime="2019-02-14T08:48:29Z">Feb 14, 2019</relative-time>
        </span>
      </div>

    <div class="Box-body d-flex flex-items-center flex-auto f6 border-bottom-0 flex-wrap" >
      <details class="details-reset details-overlay details-overlay-dark lh-default text-gray-dark float-left mr-2" id="blob_contributors_box">
        <summary class="btn-link" aria-haspopup="dialog">
          <span><strong>4</strong> contributors</span>
        </summary>
        <details-dialog
          class="Box Box--overlay d-flex flex-column anim-fade-in fast"
          aria-label="Users who have contributed to this file"
          >
          <div class="Box-header">
            <button class="Box-btn-octicon btn-octicon float-right" type="button" aria-label="Close dialog" data-close-dialog>
              <svg class="octicon octicon-x" viewBox="0 0 12 16" version="1.1" width="12" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.48 8l3.75 3.75-1.48 1.48L6 9.48l-3.75 3.75-1.48-1.48L4.52 8 .77 4.25l1.48-1.48L6 6.52l3.75-3.75 1.48 1.48L7.48 8z"/></svg>
            </button>
            <h3 class="Box-title">
              Users who have contributed to this file
            </h3>
          </div>
              <ul class="list-style-none overflow-auto">
    <li class="Box-row">
      <a class="link-gray-dark no-underline" href="/queenypingcap">
        <img class="avatar mr-1" alt="" src="https://avatars1.githubusercontent.com/u/19528243?s=40&amp;v=4" width="20" height="20" />
        queenypingcap
</a>    </li>
    <li class="Box-row">
      <a class="link-gray-dark no-underline" href="/lilin90">
        <img class="avatar mr-1" alt="" src="https://avatars1.githubusercontent.com/u/30922556?s=40&amp;v=4" width="20" height="20" />
        lilin90
</a>    </li>
    <li class="Box-row">
      <a class="link-gray-dark no-underline" href="/shenli">
        <img class="avatar mr-1" alt="" src="https://avatars2.githubusercontent.com/u/1192573?s=40&amp;v=4" width="20" height="20" />
        shenli
</a>    </li>
    <li class="Box-row">
      <a class="link-gray-dark no-underline" href="/CaitinChen">
        <img class="avatar mr-1" alt="" src="https://avatars2.githubusercontent.com/u/34535727?s=40&amp;v=4" width="20" height="20" />
        CaitinChen
</a>    </li>
</ul>

        </details-dialog>
      </details>
        <span class="d-none d-md-inline-block">
    <a class="avatar-link" data-hovercard-type="user" data-hovercard-url="/hovercards?user_id=19528243" data-octo-click="hovercard-link-click" data-octo-dimensions="link_type:self" href="/pingcap/docs-cn/commits/master/benchmark/sysbench.md?author=queenypingcap">
      <img class="avatar mr-1" src="https://avatars1.githubusercontent.com/u/19528243?s=40&amp;v=4" width="20" height="20" alt="@queenypingcap" /> 
</a>    <a class="avatar-link" data-hovercard-type="user" data-hovercard-url="/hovercards?user_id=30922556" data-octo-click="hovercard-link-click" data-octo-dimensions="link_type:self" href="/pingcap/docs-cn/commits/master/benchmark/sysbench.md?author=lilin90">
      <img class="avatar mr-1" src="https://avatars1.githubusercontent.com/u/30922556?s=40&amp;v=4" width="20" height="20" alt="@lilin90" /> 
</a>    <a class="avatar-link" data-hovercard-type="user" data-hovercard-url="/hovercards?user_id=1192573" data-octo-click="hovercard-link-click" data-octo-dimensions="link_type:self" href="/pingcap/docs-cn/commits/master/benchmark/sysbench.md?author=shenli">
      <img class="avatar mr-1" src="https://avatars2.githubusercontent.com/u/1192573?s=40&amp;v=4" width="20" height="20" alt="@shenli" /> 
</a>    <a class="avatar-link" data-hovercard-type="user" data-hovercard-url="/hovercards?user_id=34535727" data-octo-click="hovercard-link-click" data-octo-dimensions="link_type:self" href="/pingcap/docs-cn/commits/master/benchmark/sysbench.md?author=CaitinChen">
      <img class="avatar mr-1" src="https://avatars2.githubusercontent.com/u/34535727?s=40&amp;v=4" width="20" height="20" alt="@CaitinChen" /> 
</a>
</span>

    </div>
  </div>





    <div class="Box mt-3 position-relative">
      
<div class="Box-header py-2 d-flex flex-justify-between flex-items-center">

  <div class="text-mono f6">
      210 lines (161 sloc)
      <span class="file-info-divider"></span>
    7.07 KB
  </div>

  <div class="d-flex">

    <div class="BtnGroup">
      <a id="raw-url" class="btn btn-sm BtnGroup-item" href="/pingcap/docs-cn/raw/master/benchmark/sysbench.md">Raw</a>
        <a class="btn btn-sm js-update-url-with-hash BtnGroup-item" data-hotkey="b" href="/pingcap/docs-cn/blame/master/benchmark/sysbench.md">Blame</a>
      <a rel="nofollow" class="btn btn-sm BtnGroup-item" href="/pingcap/docs-cn/commits/master/benchmark/sysbench.md">History</a>
    </div>


    <div>

          <button type="button" class="btn-octicon disabled tooltipped tooltipped-nw"
            aria-label="You must be signed in to make or propose changes">
            <svg class="octicon octicon-pencil" viewBox="0 0 14 16" version="1.1" width="14" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M0 12v3h3l8-8-3-3-8 8zm3 2H1v-2h1v1h1v1zm10.3-9.3L12 6 9 3l1.3-1.3a.996.996 0 0 1 1.41 0l1.59 1.59c.39.39.39 1.02 0 1.41z"/></svg>
          </button>
          <button type="button" class="btn-octicon btn-octicon-danger disabled tooltipped tooltipped-nw"
            aria-label="You must be signed in to make or propose changes">
            <svg class="octicon octicon-trashcan" viewBox="0 0 12 16" version="1.1" width="12" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M11 2H9c0-.55-.45-1-1-1H5c-.55 0-1 .45-1 1H2c-.55 0-1 .45-1 1v1c0 .55.45 1 1 1v9c0 .55.45 1 1 1h7c.55 0 1-.45 1-1V5c.55 0 1-.45 1-1V3c0-.55-.45-1-1-1zm-1 12H3V5h1v8h1V5h1v8h1V5h1v8h1V5h1v9zm1-10H2V3h9v1z"/></svg>
          </button>
    </div>
  </div>
</div>

      
  <div id="readme" class="Box-body readme blob instapaper_body js-code-block-container">
    <article class="markdown-body entry-content p-5" itemprop="text"><table data-table-type="yaml-metadata">
  <thead>
  <tr>
  <th>title</th>
  <th>category</th>
  <th>draft</th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td><div>TiDB Sysbench 性能测试报告 - v1.0.0</div></td>
  <td><div>benchmark</div></td>
  <td><div>true</div></td>
  </tr>
  </tbody>
</table>

<h1><a id="user-content-tidb-sysbench-性能测试报告---v100" class="anchor" aria-hidden="true" href="#tidb-sysbench-性能测试报告---v100"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>TiDB Sysbench 性能测试报告 - v1.0.0</h1>
<h2><a id="user-content-测试目的" class="anchor" aria-hidden="true" href="#测试目的"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>测试目的</h2>
<p>测试 TiDB 在 OLTP 场景下的性能以及水平扩展能力。</p>
<blockquote>
<p><strong>注意</strong>: 不同的测试环境可能使测试结果发生改变。</p>
</blockquote>
<h2><a id="user-content-测试版本时间地点" class="anchor" aria-hidden="true" href="#测试版本时间地点"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>测试版本、时间、地点</h2>
<p>TiDB 版本：v1.0.0
时间：2017 年 10 月 20 日
地点：北京</p>
<h2><a id="user-content-测试环境" class="anchor" aria-hidden="true" href="#测试环境"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>测试环境</h2>
<p>IDC 机器</p>
<table>
<thead>
<tr>
<th align="center">类别</th>
<th align="center">名称</th>
</tr>
</thead>
<tbody>
<tr>
<td align="center">OS</td>
<td align="center">linux (CentOS 7.3.1611)</td>
</tr>
<tr>
<td align="center">CPU</td>
<td align="center">40 vCPUs, Intel(R) Xeon(R) CPU E5-2630 v4 @ 2.20GHz</td>
</tr>
<tr>
<td align="center">RAM</td>
<td align="center">128GB</td>
</tr>
<tr>
<td align="center">DISK</td>
<td align="center">1.5T SSD * 2  + Optane SSD * 1</td>
</tr>
</tbody>
</table>
<p>Sysbench 版本: 1.0.6</p>
<p>测试脚本: <a href="https://github.com/pingcap/tidb-bench/tree/cwen/not_prepared_statement/sysbench">https://github.com/pingcap/tidb-bench/tree/cwen/not_prepared_statement/sysbench</a></p>
<h2><a id="user-content-测试方案" class="anchor" aria-hidden="true" href="#测试方案"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>测试方案</h2>
<h3><a id="user-content-场景一sysbench-标准性能测试" class="anchor" aria-hidden="true" href="#场景一sysbench-标准性能测试"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>场景一：sysbench 标准性能测试</h3>
<p>测试表结构</p>
<pre><code>CREATE TABLE `sbtest` (
  `id` int(10) unsigned NOT NULL AUTO_INCREMENT,
  `k` int(10) unsigned NOT NULL DEFAULT '0',
  `c` char(120) NOT NULL DEFAULT '',
  `pad` char(60) NOT NULL DEFAULT '',
  PRIMARY KEY (`id`),
  KEY `k_1` (`k`)
) ENGINE=InnoDB  
</code></pre>
<p>部署方案以及配置参数</p>
<pre><code>// TiDB 部署方案
172.16.20.4    4*tikv    1*tidb    1*sysbench
172.16.20.6    4*tikv    1*tidb    1*sysbench
172.16.20.7    4*tikv    1*tidb    1*sysbench
172.16.10.8    1*tidb    1*pd      1*sysbench  

// 每个物理节点有三块盘：
data3: 2 tikv  (Optane SSD)
data2: 1 tikv
data1: 1 tikv

// TiKV 参数配置
sync-log = false
grpc-concurrency = 8
grpc-raft-conn-num = 24
[defaultcf]
block-cache-size = "12GB"
[writecf]
block-cache-size = "5GB"
[raftdb.defaultcf]
block-cache-size = "2GB"

// Mysql 部署方案
// 分别使用半同步复制和异步复制，部署两副本
172.16.20.4    master
172.16.20.6    slave
172.16.20.7    slave
172.16.10.8    1*sysbench
Mysql version: 5.6.37

// Mysql 参数配置
thread_cache_size = 64
innodb_buffer_pool_size = 64G
innodb_file_per_table = 1
innodb_flush_log_at_trx_commit = 0  
datadir = /data3/mysql  
max_connections = 2000
</code></pre>
<ul>
<li>标准 oltp 测试</li>
</ul>
<table>
<thead>
<tr>
<th align="center">-</th>
<th align="center">table count</th>
<th align="center">table size</th>
<th align="center">sysbench threads</th>
<th align="center">tps</th>
<th align="center">qps</th>
<th align="center">latency(avg / .95)</th>
</tr>
</thead>
<tbody>
<tr>
<td align="center">TiDB</td>
<td align="center">32</td>
<td align="center">100 万</td>
<td align="center">64 * 4</td>
<td align="center">3834</td>
<td align="center">76692</td>
<td align="center">67.04 ms / 110.88 ms</td>
</tr>
<tr>
<td align="center">TiDB</td>
<td align="center">32</td>
<td align="center">100 万</td>
<td align="center">128 * 4</td>
<td align="center">4172</td>
<td align="center">83459</td>
<td align="center">124.00 ms / 194.21 ms</td>
</tr>
<tr>
<td align="center">TiDB</td>
<td align="center">32</td>
<td align="center">100 万</td>
<td align="center">256 * 4</td>
<td align="center">4577</td>
<td align="center">91547</td>
<td align="center">228.36 ms / 334.02 ms</td>
</tr>
<tr>
<td align="center">TiDB</td>
<td align="center">32</td>
<td align="center">500 万</td>
<td align="center">256 * 4</td>
<td align="center">4032</td>
<td align="center">80657</td>
<td align="center">256.62 ms / 443.88 ms</td>
</tr>
<tr>
<td align="center">TiDB</td>
<td align="center">32</td>
<td align="center">1000 万</td>
<td align="center">256 * 4</td>
<td align="center">3811</td>
<td align="center">76233</td>
<td align="center">269.46 ms / 505.20 ms</td>
</tr>
<tr>
<td align="center">Mysql</td>
<td align="center">32</td>
<td align="center">100 万</td>
<td align="center">64</td>
<td align="center">2392</td>
<td align="center">47845</td>
<td align="center">26.75 ms / 73.13 ms</td>
</tr>
<tr>
<td align="center">Mysql</td>
<td align="center">32</td>
<td align="center">100 万</td>
<td align="center">128</td>
<td align="center">2493</td>
<td align="center">49874</td>
<td align="center">51.32 ms / 173.58 ms</td>
</tr>
<tr>
<td align="center">Mysql</td>
<td align="center">32</td>
<td align="center">100 万</td>
<td align="center">256</td>
<td align="center">2561</td>
<td align="center">51221</td>
<td align="center">99.95 ms  / 287.38 ms</td>
</tr>
<tr>
<td align="center">Mysql</td>
<td align="center">32</td>
<td align="center">500 万</td>
<td align="center">256</td>
<td align="center">1902</td>
<td align="center">38045</td>
<td align="center">134.56 ms / 363.18 ms</td>
</tr>
<tr>
<td align="center">Mysql</td>
<td align="center">32</td>
<td align="center">1000 万</td>
<td align="center">256</td>
<td align="center">1770</td>
<td align="center">35416</td>
<td align="center">144.55 ms / 383.33 ms</td>
</tr>
</tbody>
</table>
<p><a target="_blank" rel="noopener noreferrer" href="https://camo.githubusercontent.com/ff117abd6c76d0815bbdd51ec796092fd530a475/687474703a2f2f37786e7030322e636f6d312e7a302e676c622e636c6f7564646e2e636f6d2f746872656164735f6f6c74702e706e673f696d61676556696577322f322f772f3730302f712f3735253743696d616765736c696d"><img src="https://camo.githubusercontent.com/ff117abd6c76d0815bbdd51ec796092fd530a475/687474703a2f2f37786e7030322e636f6d312e7a302e676c622e636c6f7564646e2e636f6d2f746872656164735f6f6c74702e706e673f696d61676556696577322f322f772f3730302f712f3735253743696d616765736c696d" alt="" data-canonical-src="http://7xnp02.com1.z0.glb.clouddn.com/threads_oltp.png?imageView2/2/w/700/q/75%7Cimageslim" style="max-width:100%;"></a></p>
<p><a target="_blank" rel="noopener noreferrer" href="https://camo.githubusercontent.com/6da0279a6b0f48478bc9c33781b2f6a64bfbe2ef/687474703a2f2f37786e7030322e636f6d312e7a302e676c622e636c6f7564646e2e636f6d2f7461626c655f73697a655f6f6c74702e706e673f696d61676556696577322f322f772f3730302f712f3735253743696d616765736c696d"><img src="https://camo.githubusercontent.com/6da0279a6b0f48478bc9c33781b2f6a64bfbe2ef/687474703a2f2f37786e7030322e636f6d312e7a302e676c622e636c6f7564646e2e636f6d2f7461626c655f73697a655f6f6c74702e706e673f696d61676556696577322f322f772f3730302f712f3735253743696d616765736c696d" alt="" data-canonical-src="http://7xnp02.com1.z0.glb.clouddn.com/table_size_oltp.png?imageView2/2/w/700/q/75%7Cimageslim" style="max-width:100%;"></a></p>
<ul>
<li>标准 select 测试</li>
</ul>
<table>
<thead>
<tr>
<th align="center">-</th>
<th align="center">table count</th>
<th align="center">table size</th>
<th align="center">sysbench threads</th>
<th align="center">qps</th>
<th align="center">latency(avg / .95)</th>
</tr>
</thead>
<tbody>
<tr>
<td align="center">TiDB</td>
<td align="center">32</td>
<td align="center">100 万</td>
<td align="center">64 * 4</td>
<td align="center">160299</td>
<td align="center">1.61ms / 50.06 ms</td>
</tr>
<tr>
<td align="center">TiDB</td>
<td align="center">32</td>
<td align="center">100 万</td>
<td align="center">128 * 4</td>
<td align="center">183347</td>
<td align="center">2.85 ms / 8.66 ms</td>
</tr>
<tr>
<td align="center">TiDB</td>
<td align="center">32</td>
<td align="center">100 万</td>
<td align="center">256 * 4</td>
<td align="center">196515</td>
<td align="center">5.42 ms / 14.43 ms</td>
</tr>
<tr>
<td align="center">TiDB</td>
<td align="center">32</td>
<td align="center">500 万</td>
<td align="center">256 * 4</td>
<td align="center">187628</td>
<td align="center">5.66 ms / 15.04 ms</td>
</tr>
<tr>
<td align="center">TiDB</td>
<td align="center">32</td>
<td align="center">1000 万</td>
<td align="center">256 * 4</td>
<td align="center">187440</td>
<td align="center">5.65 ms / 15.37 ms</td>
</tr>
<tr>
<td align="center">Mysql</td>
<td align="center">32</td>
<td align="center">100 万</td>
<td align="center">64</td>
<td align="center">359572</td>
<td align="center">0.18 ms /  0.45 ms</td>
</tr>
<tr>
<td align="center">Mysql</td>
<td align="center">32</td>
<td align="center">100 万</td>
<td align="center">128</td>
<td align="center">410426</td>
<td align="center">0.31 ms / 0.74 ms</td>
</tr>
<tr>
<td align="center">Mysql</td>
<td align="center">32</td>
<td align="center">100 万</td>
<td align="center">256</td>
<td align="center">396867</td>
<td align="center">0.64 ms / 1.58 ms</td>
</tr>
<tr>
<td align="center">Mysql</td>
<td align="center">32</td>
<td align="center">500 万</td>
<td align="center">256</td>
<td align="center">386866</td>
<td align="center">0.66 ms / 1.64 ms</td>
</tr>
<tr>
<td align="center">Mysql</td>
<td align="center">32</td>
<td align="center">1000 万</td>
<td align="center">256</td>
<td align="center">388273</td>
<td align="center">0.66 ms / 1.64 ms</td>
</tr>
</tbody>
</table>
<p><a target="_blank" rel="noopener noreferrer" href="https://camo.githubusercontent.com/f6f67713e2dd54be786f10e905a1c95857dc6b0f/687474703a2f2f37786e7030322e636f6d312e7a302e676c622e636c6f7564646e2e636f6d2f746872656164735f73656c6563742e706e673f696d61676556696577322f322f772f3730302f712f3735253743696d616765736c696d"><img src="https://camo.githubusercontent.com/f6f67713e2dd54be786f10e905a1c95857dc6b0f/687474703a2f2f37786e7030322e636f6d312e7a302e676c622e636c6f7564646e2e636f6d2f746872656164735f73656c6563742e706e673f696d61676556696577322f322f772f3730302f712f3735253743696d616765736c696d" alt="" data-canonical-src="http://7xnp02.com1.z0.glb.clouddn.com/threads_select.png?imageView2/2/w/700/q/75%7Cimageslim" style="max-width:100%;"></a></p>
<p><a target="_blank" rel="noopener noreferrer" href="https://camo.githubusercontent.com/04c72a7d557cfc96e08242f07c1c389a11fb38bd/687474703a2f2f37786e7030322e636f6d312e7a302e676c622e636c6f7564646e2e636f6d2f7461626c655f73697a655f73656c6563742e706e673f696d61676556696577322f322f772f3730302f712f3735253743696d616765736c696d"><img src="https://camo.githubusercontent.com/04c72a7d557cfc96e08242f07c1c389a11fb38bd/687474703a2f2f37786e7030322e636f6d312e7a302e676c622e636c6f7564646e2e636f6d2f7461626c655f73697a655f73656c6563742e706e673f696d61676556696577322f322f772f3730302f712f3735253743696d616765736c696d" alt="" data-canonical-src="http://7xnp02.com1.z0.glb.clouddn.com/table_size_select.png?imageView2/2/w/700/q/75%7Cimageslim" style="max-width:100%;"></a></p>
<ul>
<li>标准 insert 测试</li>
</ul>
<table>
<thead>
<tr>
<th align="center">-</th>
<th align="center">table count</th>
<th align="center">table size</th>
<th align="center">sysbench threads</th>
<th align="center">qps</th>
<th align="center">latency(avg / .95)</th>
</tr>
</thead>
<tbody>
<tr>
<td align="center">TiDB</td>
<td align="center">32</td>
<td align="center">100 万</td>
<td align="center">64 * 4</td>
<td align="center">25308</td>
<td align="center">10.12 ms / 25.40 ms</td>
</tr>
<tr>
<td align="center">TiDB</td>
<td align="center">32</td>
<td align="center">100 万</td>
<td align="center">128 * 4</td>
<td align="center">28773</td>
<td align="center">17.80 ms / 44.58 ms</td>
</tr>
<tr>
<td align="center">TiDB</td>
<td align="center">32</td>
<td align="center">100 万</td>
<td align="center">256 * 4</td>
<td align="center">32641</td>
<td align="center">31.38 ms / 73.47 ms</td>
</tr>
<tr>
<td align="center">TiDB</td>
<td align="center">32</td>
<td align="center">500 万</td>
<td align="center">256 * 4</td>
<td align="center">30430</td>
<td align="center">33.65 ms / 79.32 ms</td>
</tr>
<tr>
<td align="center">TiDB</td>
<td align="center">32</td>
<td align="center">1000 万</td>
<td align="center">256 * 4</td>
<td align="center">28925</td>
<td align="center">35.41 ms / 78.96 ms</td>
</tr>
<tr>
<td align="center">Mysql</td>
<td align="center">32</td>
<td align="center">100 万</td>
<td align="center">64</td>
<td align="center">14806</td>
<td align="center">4.32 ms / 9.39 ms</td>
</tr>
<tr>
<td align="center">Mysql</td>
<td align="center">32</td>
<td align="center">100 万</td>
<td align="center">128</td>
<td align="center">14884</td>
<td align="center">8.58  ms / 21.11 ms</td>
</tr>
<tr>
<td align="center">Mysql</td>
<td align="center">32</td>
<td align="center">100 万</td>
<td align="center">256</td>
<td align="center">14508</td>
<td align="center">17.64 ms / 44.98 ms</td>
</tr>
<tr>
<td align="center">Mysql</td>
<td align="center">32</td>
<td align="center">500 万</td>
<td align="center">256</td>
<td align="center">10593</td>
<td align="center">24.16 ms / 82.96 ms</td>
</tr>
<tr>
<td align="center">Mysql</td>
<td align="center">32</td>
<td align="center">1000 万</td>
<td align="center">256</td>
<td align="center">9813</td>
<td align="center">26.08 ms / 94.10 ms</td>
</tr>
</tbody>
</table>
<p><a target="_blank" rel="noopener noreferrer" href="https://camo.githubusercontent.com/6e554592f16165ec4aa1ca15239d0d4dceb0d7c4/687474703a2f2f37786e7030322e636f6d312e7a302e676c622e636c6f7564646e2e636f6d2f746872656164735f696e736572742e706e673f696d61676556696577322f322f772f3730302f712f3735253743696d616765736c696d"><img src="https://camo.githubusercontent.com/6e554592f16165ec4aa1ca15239d0d4dceb0d7c4/687474703a2f2f37786e7030322e636f6d312e7a302e676c622e636c6f7564646e2e636f6d2f746872656164735f696e736572742e706e673f696d61676556696577322f322f772f3730302f712f3735253743696d616765736c696d" alt="" data-canonical-src="http://7xnp02.com1.z0.glb.clouddn.com/threads_insert.png?imageView2/2/w/700/q/75%7Cimageslim" style="max-width:100%;"></a></p>
<p><a target="_blank" rel="noopener noreferrer" href="https://camo.githubusercontent.com/84fed981fba5c0198255969f5904466134fcfb1b/687474703a2f2f37786e7030322e636f6d312e7a302e676c622e636c6f7564646e2e636f6d2f7461626c655f73697a655f696e736572742e706e673f696d61676556696577322f322f772f3730302f712f3735253743696d616765736c696d"><img src="https://camo.githubusercontent.com/84fed981fba5c0198255969f5904466134fcfb1b/687474703a2f2f37786e7030322e636f6d312e7a302e676c622e636c6f7564646e2e636f6d2f7461626c655f73697a655f696e736572742e706e673f696d61676556696577322f322f772f3730302f712f3735253743696d616765736c696d" alt="" data-canonical-src="http://7xnp02.com1.z0.glb.clouddn.com/table_size_insert.png?imageView2/2/w/700/q/75%7Cimageslim" style="max-width:100%;"></a></p>
<h3><a id="user-content-场景二tidb-水平扩展能力测试" class="anchor" aria-hidden="true" href="#场景二tidb-水平扩展能力测试"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>场景二：TiDB 水平扩展能力测试</h3>
<p>部署方案以及配置参数</p>
<pre><code>// TiDB 部署方案
172.16.20.3    4*tikv
172.16.10.2    1*tidb    1*pd     1*sysbench

每个物理节点有三块盘：
data3: 2 tikv  (Optane SSD)
data2: 1 tikv
data1: 1 tikv

// TiKV 参数配置
sync-log = false
grpc-concurrency = 8
grpc-raft-conn-num = 24
[defaultcf]
block-cache-size = "12GB"
[writecf]
block-cache-size = "5GB"
[raftdb.defaultcf]
block-cache-size = "2GB"
</code></pre>
<ul>
<li>标准 oltp 测试</li>
</ul>
<table>
<thead>
<tr>
<th align="center">-</th>
<th align="center">table count</th>
<th align="center">table size</th>
<th align="center">sysbench threads</th>
<th align="center">tps</th>
<th align="center">qps</th>
<th align="center">latency(avg / .95)</th>
</tr>
</thead>
<tbody>
<tr>
<td align="center">1 物理节点 TiDB</td>
<td align="center">32</td>
<td align="center">100 万</td>
<td align="center">256 * 1</td>
<td align="center">2495</td>
<td align="center">49902</td>
<td align="center">102.42 ms / 125.52 ms</td>
</tr>
<tr>
<td align="center">2 物理节点 TiDB</td>
<td align="center">32</td>
<td align="center">100 万</td>
<td align="center">256 * 2</td>
<td align="center">5007</td>
<td align="center">100153</td>
<td align="center">102.23 ms / 125.52 ms</td>
</tr>
<tr>
<td align="center">4 物理节点 TiDB</td>
<td align="center">32</td>
<td align="center">100 万</td>
<td align="center">256 * 4</td>
<td align="center">8984</td>
<td align="center">179692</td>
<td align="center">114.96 ms / 176.73 ms</td>
</tr>
<tr>
<td align="center">6 物理节点 TiDB</td>
<td align="center">32</td>
<td align="center">500 万</td>
<td align="center">256 * 6</td>
<td align="center">12953</td>
<td align="center">259072</td>
<td align="center">117.80 ms / 200.47 ms</td>
</tr>
</tbody>
</table>
<p><a target="_blank" rel="noopener noreferrer" href="https://camo.githubusercontent.com/08ebaf0bfd2bef7033b7df48682ac9eaeb4fbe38/687474703a2f2f37786e7030322e636f6d312e7a302e676c622e636c6f7564646e2e636f6d2f7363616c655f746964625f6f6c74702e706e673f696d61676556696577322f322f772f3730302f712f3735253743696d616765736c696d"><img src="https://camo.githubusercontent.com/08ebaf0bfd2bef7033b7df48682ac9eaeb4fbe38/687474703a2f2f37786e7030322e636f6d312e7a302e676c622e636c6f7564646e2e636f6d2f7363616c655f746964625f6f6c74702e706e673f696d61676556696577322f322f772f3730302f712f3735253743696d616765736c696d" alt="" data-canonical-src="http://7xnp02.com1.z0.glb.clouddn.com/scale_tidb_oltp.png?imageView2/2/w/700/q/75%7Cimageslim" style="max-width:100%;"></a></p>
<ul>
<li>标准 select 测试</li>
</ul>
<table>
<thead>
<tr>
<th align="center">-</th>
<th align="center">table count</th>
<th align="center">table size</th>
<th align="center">sysbench threads</th>
<th align="center">qps</th>
<th align="center">latency(avg / .95)</th>
</tr>
</thead>
<tbody>
<tr>
<td align="center">1 物理节点 TiDB</td>
<td align="center">32</td>
<td align="center">100 万</td>
<td align="center">256 * 1</td>
<td align="center">71841</td>
<td align="center">3.56 ms / 8.74 ms</td>
</tr>
<tr>
<td align="center">2 物理节点 TiDB</td>
<td align="center">32</td>
<td align="center">100 万</td>
<td align="center">256 * 2</td>
<td align="center">146615</td>
<td align="center">3.49 ms / 8.74 ms</td>
</tr>
<tr>
<td align="center">4 物理节点 TiDB</td>
<td align="center">32</td>
<td align="center">100 万</td>
<td align="center">256 * 4</td>
<td align="center">289933</td>
<td align="center">3.53 ms / 8.74 ms</td>
</tr>
<tr>
<td align="center">6 物理节点 TiDB</td>
<td align="center">32</td>
<td align="center">500 万</td>
<td align="center">256 * 6</td>
<td align="center">435313</td>
<td align="center">3.55 ms / 9.17 ms</td>
</tr>
</tbody>
</table>
<p><a target="_blank" rel="noopener noreferrer" href="https://camo.githubusercontent.com/5d044aa9f725719c32bd4e4b0b218ddbec2e9aa6/687474703a2f2f37786e7030322e636f6d312e7a302e676c622e636c6f7564646e2e636f6d2f7363616c655f746964625f73656c6563742e706e673f696d61676556696577322f322f772f3730302f712f3735253743696d616765736c696d"><img src="https://camo.githubusercontent.com/5d044aa9f725719c32bd4e4b0b218ddbec2e9aa6/687474703a2f2f37786e7030322e636f6d312e7a302e676c622e636c6f7564646e2e636f6d2f7363616c655f746964625f73656c6563742e706e673f696d61676556696577322f322f772f3730302f712f3735253743696d616765736c696d" alt="" data-canonical-src="http://7xnp02.com1.z0.glb.clouddn.com/scale_tidb_select.png?imageView2/2/w/700/q/75%7Cimageslim" style="max-width:100%;"></a></p>
<ul>
<li>标准 insert 测试</li>
</ul>
<table>
<thead>
<tr>
<th align="center">-</th>
<th align="center">table count</th>
<th align="center">table size</th>
<th align="center">sysbench threads</th>
<th align="center">qps</th>
<th align="center">latency(avg / .95)</th>
</tr>
</thead>
<tbody>
<tr>
<td align="center">3 物理节点 TiKV</td>
<td align="center">32</td>
<td align="center">100 万</td>
<td align="center">256 * 3</td>
<td align="center">40547</td>
<td align="center">18.93 ms / 38.25 ms</td>
</tr>
<tr>
<td align="center">5 物理节点 TiKV</td>
<td align="center">32</td>
<td align="center">100 万</td>
<td align="center">256 * 3</td>
<td align="center">60689</td>
<td align="center">37.96 ms / 29.9 ms</td>
</tr>
<tr>
<td align="center">7 物理节点 TiKV</td>
<td align="center">32</td>
<td align="center">100 万</td>
<td align="center">256 * 3</td>
<td align="center">80087</td>
<td align="center">9.62 ms / 21.37 ms</td>
</tr>
</tbody>
</table>
<p><a target="_blank" rel="noopener noreferrer" href="https://camo.githubusercontent.com/331659ed4d0cc810ae3d4d0155e17993d59fabc1/687474703a2f2f37786e7030322e636f6d312e7a302e676c622e636c6f7564646e2e636f6d2f7363616c655f74696b765f696e736572742e706e673f696d61676556696577322f322f772f3730302f712f3735253743696d616765736c696d"><img src="https://camo.githubusercontent.com/331659ed4d0cc810ae3d4d0155e17993d59fabc1/687474703a2f2f37786e7030322e636f6d312e7a302e676c622e636c6f7564646e2e636f6d2f7363616c655f74696b765f696e736572742e706e673f696d61676556696577322f322f772f3730302f712f3735253743696d616765736c696d" alt="" data-canonical-src="http://7xnp02.com1.z0.glb.clouddn.com/scale_tikv_insert.png?imageView2/2/w/700/q/75%7Cimageslim" style="max-width:100%;"></a></p>
</article>
  </div>

    </div>

  

  <details class="details-reset details-overlay details-overlay-dark">
    <summary data-hotkey="l" aria-label="Jump to line"></summary>
    <details-dialog class="Box Box--overlay d-flex flex-column anim-fade-in fast linejump" aria-label="Jump to line">
      <!-- '"` --><!-- </textarea></xmp> --></option></form><form class="js-jump-to-line-form Box-body d-flex" action="" accept-charset="UTF-8" method="get"><input name="utf8" type="hidden" value="&#x2713;" />
        <input class="form-control flex-auto mr-3 linejump-input js-jump-to-line-field" type="text" placeholder="Jump to line&hellip;" aria-label="Jump to line" autofocus>
        <button type="submit" class="btn" data-close-dialog>Go</button>
</form>    </details-dialog>
  </details>



  </div>
  <div class="modal-backdrop js-touch-events"></div>
</div>

    </main>
  </div>
  

  </div>

        
<div class="footer container-lg width-full px-3" role="contentinfo">
  <div class="position-relative d-flex flex-justify-between pt-6 pb-2 mt-6 f6 text-gray border-top border-gray-light ">
    <ul class="list-style-none d-flex flex-wrap ">
      <li class="mr-3">&copy; 2019 <span title="0.24641s from unicorn-7575ff56bd-z7vck">GitHub</span>, Inc.</li>
        <li class="mr-3"><a data-ga-click="Footer, go to terms, text:terms" href="https://github.com/site/terms">Terms</a></li>
        <li class="mr-3"><a data-ga-click="Footer, go to privacy, text:privacy" href="https://github.com/site/privacy">Privacy</a></li>
        <li class="mr-3"><a data-ga-click="Footer, go to security, text:security" href="https://github.com/security">Security</a></li>
        <li class="mr-3"><a href="https://githubstatus.com/" data-ga-click="Footer, go to status, text:status">Status</a></li>
        <li><a data-ga-click="Footer, go to help, text:help" href="https://help.github.com">Help</a></li>
    </ul>

    <a aria-label="Homepage" title="GitHub" class="footer-octicon mx-lg-4" href="https://github.com">
      <svg height="24" class="octicon octicon-mark-github" viewBox="0 0 16 16" version="1.1" width="24" aria-hidden="true"><path fill-rule="evenodd" d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0 0 16 8c0-4.42-3.58-8-8-8z"/></svg>
</a>
   <ul class="list-style-none d-flex flex-wrap ">
        <li class="mr-3"><a data-ga-click="Footer, go to contact, text:contact" href="https://github.com/contact">Contact GitHub</a></li>
        <li class="mr-3"><a href="https://github.com/pricing" data-ga-click="Footer, go to Pricing, text:Pricing">Pricing</a></li>
      <li class="mr-3"><a href="https://developer.github.com" data-ga-click="Footer, go to api, text:api">API</a></li>
      <li class="mr-3"><a href="https://training.github.com" data-ga-click="Footer, go to training, text:training">Training</a></li>
        <li class="mr-3"><a href="https://github.blog" data-ga-click="Footer, go to blog, text:blog">Blog</a></li>
        <li><a data-ga-click="Footer, go to about, text:about" href="https://github.com/about">About</a></li>

    </ul>
  </div>
  <div class="d-flex flex-justify-center pb-6">
    <span class="f6 text-gray-light"></span>
  </div>
</div>



  <div id="ajax-error-message" class="ajax-error-message flash flash-error">
    <svg class="octicon octicon-alert" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M8.893 1.5c-.183-.31-.52-.5-.887-.5s-.703.19-.886.5L.138 13.499a.98.98 0 0 0 0 1.001c.193.31.53.501.886.501h13.964c.367 0 .704-.19.877-.5a1.03 1.03 0 0 0 .01-1.002L8.893 1.5zm.133 11.497H6.987v-2.003h2.039v2.003zm0-3.004H6.987V5.987h2.039v4.006z"/></svg>
    <button type="button" class="flash-close js-ajax-error-dismiss" aria-label="Dismiss error">
      <svg class="octicon octicon-x" viewBox="0 0 12 16" version="1.1" width="12" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.48 8l3.75 3.75-1.48 1.48L6 9.48l-3.75 3.75-1.48-1.48L4.52 8 .77 4.25l1.48-1.48L6 6.52l3.75-3.75 1.48 1.48L7.48 8z"/></svg>
    </button>
    You can’t perform that action at this time.
  </div>


    <script crossorigin="anonymous" integrity="sha512-5g98V2j8YTLsw7llCJHOsXoeKDJzBaS1EPqZe/YOBBiPXDE/+5S1WkRoX6AVs/hXTzyJGB3x95OKNDat4vpk0A==" type="application/javascript" src="https://github.githubassets.com/assets/compat-bootstrap-3ee7f90c.js"></script>
    <script crossorigin="anonymous" integrity="sha512-NrjCh49VLw2768XCSxbHHsu05NjXH1bEbBxduYC8V1OW7L9fK7jF2OrX3dyplx4IwphXOPSbTAd8zuqHBGN59g==" type="application/javascript" src="https://github.githubassets.com/assets/frameworks-40c99db0.js"></script>
    
    <script crossorigin="anonymous" async="async" integrity="sha512-snJoZf7iE5XLYSKo0uIPSbiNcFv5GBWCqsmEJ45YOjuEg5/fbC2/TJmlDC+AP385edNejDa/LbDaiPff+8zvPQ==" type="application/javascript" src="https://github.githubassets.com/assets/github-bootstrap-07e85729.js"></script>
    
    
    
  <div class="js-stale-session-flash stale-session-flash flash flash-warn flash-banner" hidden
    >
    <svg class="octicon octicon-alert" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M8.893 1.5c-.183-.31-.52-.5-.887-.5s-.703.19-.886.5L.138 13.499a.98.98 0 0 0 0 1.001c.193.31.53.501.886.501h13.964c.367 0 .704-.19.877-.5a1.03 1.03 0 0 0 .01-1.002L8.893 1.5zm.133 11.497H6.987v-2.003h2.039v2.003zm0-3.004H6.987V5.987h2.039v4.006z"/></svg>
    <span class="signed-in-tab-flash">You signed in with another tab or window. <a href="">Reload</a> to refresh your session.</span>
    <span class="signed-out-tab-flash">You signed out in another tab or window. <a href="">Reload</a> to refresh your session.</span>
  </div>
  <template id="site-details-dialog">
  <details class="details-reset details-overlay details-overlay-dark lh-default text-gray-dark" open>
    <summary aria-haspopup="dialog" aria-label="Close dialog"></summary>
    <details-dialog class="Box Box--overlay d-flex flex-column anim-fade-in fast">
      <button class="Box-btn-octicon m-0 btn-octicon position-absolute right-0 top-0" type="button" aria-label="Close dialog" data-close-dialog>
        <svg class="octicon octicon-x" viewBox="0 0 12 16" version="1.1" width="12" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.48 8l3.75 3.75-1.48 1.48L6 9.48l-3.75 3.75-1.48-1.48L4.52 8 .77 4.25l1.48-1.48L6 6.52l3.75-3.75 1.48 1.48L7.48 8z"/></svg>
      </button>
      <div class="octocat-spinner my-6 js-details-dialog-spinner"></div>
    </details-dialog>
  </details>
</template>

  <div class="Popover js-hovercard-content position-absolute" style="display: none; outline: none;" tabindex="0">
  <div class="Popover-message Popover-message--bottom-left Popover-message--large Box box-shadow-large" style="width:360px;">
  </div>
</div>

  <div aria-live="polite" class="js-global-screen-reader-notice sr-only"></div>

  </body>
</html>

