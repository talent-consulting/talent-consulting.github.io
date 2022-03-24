___
category: guides
type: index 
___

<div class="grid is-fibonacci">
    {% for item in page.items %}
    <div class="grid-item">
        <div class="columns is-mobile is-gapless has-box-shadow-heavy has-border-radius-large has-overflow-hidden is-relative"
            data-bi-name="card">
            <div class="column is-4">
                <div class="is-flex has-flex-align-items-center has-flex-justify-content-center is-full-height"
                    style="background-color: #00518F;">
                    <span aria-hidden="true">
                        <i class="{{ item.icon }}"></i>
                    </span>
                </div>
            </div>
            <div class="column is-8 has-body-background">
                <div class="has-padding-medium">
                    <a href="{{ item.url | relative_url }}"  class="is-block stretched-link" data-linktype="absolute-path">
                        <h2 id="{{ item.title | remove: ' ' }}" class="is-size-large">{{ item.title }}</h2>
                    </a>
                </div>
            </div>
        </div>
    </div>
    {% endfor %}
</div>

<div>
    <div class="grid is-fibonacci">
        <div class="grid-item">
            <div class="columns is-mobile is-gapless has-box-shadow-heavy has-border-radius-large has-overflow-hidden is-relative"
                data-bi-name="card">
                <div class="column is-4">
                    <div class="is-flex has-flex-align-items-center has-flex-justify-content-center is-full-height"
                        style="background-color: #0091FF;">
                        <span aria-hidden="true">
                            <i class="fas fa-toolbox fa-2x"></i>
                        </span>
                    </div>
                </div>
                <div class="column is-8 has-body-background">
                    <div class="has-padding-medium">
                        <a href="/strategies/" class='is-block stretched-link' data-linktype='absolute-path'>
                            <h3 id="architecture" class='is-size-large'>
                                Strategy & Architecture
                            </h3>
                        </a>
                        <p class="is-size-small has-line-height-reset has-text-subtle has-margin-top-small">
                            <strong>General</strong> architectural and strategic documentation.
                        </p>
                    </div>
                </div>
            </div>
        </div>
                <div class="grid-item">
            <div class="columns is-mobile is-gapless has-box-shadow-heavy has-border-radius-large has-overflow-hidden is-relative"
               data-bi-name="card">
                <div class="column is-4">
                    <div class="is-flex has-flex-align-items-center has-flex-justify-content-center is-full-height"
                        style="background-color: #0091FF;">
                        <span aria-hidden="true">
                            <i class="fas fa-check-circle fa-2x"></i>
                        </span>
                    </div>
                </div>
                <div class="column is-8 has-body-background">
                    <div class="has-padding-medium">
                        <a href="/standards/" class='is-block stretched-link' data-linktype='absolute-path'>
                            <h3 id="standards" class='is-size-large'>
                                General Platform Standards
                            </h3>
                        </a>
                        <p class="is-size-small has-line-height-reset has-text-subtle has-margin-top-small">
                            <strong>General</strong> standards (naming etc.).
                        </p>
                    </div>
                </div>
            </div>
        </div>
        <div class="grid-item">
            <div class="columns is-mobile is-gapless has-box-shadow-heavy has-border-radius-large has-overflow-hidden is-relative"
                data-bi-name="card">
                <div class="column is-4">
                    <div class="is-flex has-flex-align-items-center has-flex-justify-content-center is-full-height"
                        style="background-color: #0091FF;">
                        <span aria-hidden="true">
                            <i class="fas fa-book-open fa-2x"></i>
                        </span>
                    </div>
                </div>
                <div class="column is-8 has-body-background">
                    <div class="has-padding-medium">
                        <a href="/rfcs/" class='is-block stretched-link' data-linktype='absolute-path'>
                            <h3 id="rfcs" class='is-size-large'>
                                RFCs
                            </h3>
                        </a>
                        <p class="is-size-small has-line-height-reset has-text-subtle has-margin-top-small">
                            <strong>Read</strong> the latest RFC documentation.
                        </p>
                    </div>
                </div>
            </div>
        </div>
                <div class="grid-item">
            <div class="columns is-mobile is-gapless has-box-shadow-heavy has-border-radius-large has-overflow-hidden is-relative"
                data-bi-name="card">
                <div class="column is-4">
                    <div class="is-flex has-flex-align-items-center has-flex-justify-content-center is-full-height"
                        style="background-color: #0091FF;">
                        <span aria-hidden="true">
                            <i class="fas fa-handshake fa-2x"></i>
                        </span>
                    </div>
                </div>
                <div class="column is-8 has-body-background">
                    <div class="has-padding-medium">
                        <a href="/meetingsPublications/" class='is-block stretched-link' data-linktype='absolute-path'>
                            <h3 id="meetingsPublications" class='is-size-large'>
                                Meetings & Publications
                            </h3>
                        </a>
                        <p class="is-size-small has-line-height-reset has-text-subtle has-margin-top-small">
                            <strong>Browse</strong> meeting literature / KITs / presentation material, produced by CPC.
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>
 
---
 
## Getting Started
 
The following sections information that is useful to new users of the environment:
 
---
 
<div>
    <div class="grid is-fibonacci">
        <div class="grid-item">
            <div class="columns is-mobile is-gapless has-box-shadow-heavy has-border-radius-large has-overflow-hidden is-relative"
                data-bi-name="card">
                <div class="column is-4">
                    <div class="is-flex has-flex-align-items-center has-flex-justify-content-center is-full-height"
                        style="background-color: #84D784;">
                        <span aria-hidden="true">
                            <i class="fas fa-play fa-2x"></i>
                        </span>
                    </div>
                </div>
                <div class="column is-8 has-body-background">
                    <div class="has-padding-medium">
                        <a href="/gettingStarted/" class='is-block stretched-link' data-linktype='absolute-path'>
                            <h3 id="gettingStarted" class='is-size-small'>
                                Getting Started
                            </h3>
                        </a>
                    </div>
                </div>
            </div>
        </div>
        <div class="grid-item">
            <div class="columns is-mobile is-gapless has-box-shadow-heavy has-border-radius-large has-overflow-hidden is-relative"
                data-bi-name="card">
                <div class="column is-4">
                    <div class="is-flex has-flex-align-items-center has-flex-justify-content-center is-full-height"
                        style="background-color: #84D784;">
                        <span aria-hidden="true">
                            <i class="fas fa-headset fa-2x"></i>
                        </span>
                    </div>
                </div>
                <div class="column is-8 has-body-background">
                    <div class="has-padding-medium">
                        <a href="/support/" class='is-block stretched-link' data-linktype='absolute-path'>
                            <h3 id="support" class='is-size-small'>
                                Support and Queries
                            </h3>
                        </a>
                    </div>
                </div>
            </div>
        </div>
        <div class="grid-item">
            <div class="columns is-mobile is-gapless has-box-shadow-heavy has-border-radius-large has-overflow-hidden is-relative"
                data-bi-name="card">
                <div class="column is-4">
                    <div class="is-flex has-flex-align-items-center has-flex-justify-content-center is-full-height"
                        style="background-color: #84D784;">
                        <span aria-hidden="true">
                            <i class="fab fa-connectdevelop fa-2x"></i>
                        </span>
                    </div>
                </div>
                <div class="column is-8 has-body-background">
                    <div class="has-padding-medium">
                        <a href="/connectivityandfirewalls/" class='is-block stretched-link' data-linktype='absolute-path'>
                            <h3 id="connectivity" class='is-size-small'>
                                Connectivity and Firewalls
                            </h3>
                        </a>
                    </div>
                </div>
            </div>
        </div>
        <div class="grid-item">
            <div class="columns is-mobile is-gapless has-box-shadow-heavy has-border-radius-large has-overflow-hidden is-relative"
                data-bi-name="card">
                <div class="column is-4">
                    <div class="is-flex has-flex-align-items-center has-flex-justify-content-center is-full-height"
                        style="background-color: #84D784;">
                        <span aria-hidden="true">
                            <i class="fas fa-file-contract fa-2x"></i>
                        </span>
                    </div>
                </div>
                <div class="column is-8 has-body-background">
                    <div class="has-padding-medium">
                        <a href="/terms/" class='is-block stretched-link' data-linktype='absolute-path'>
                            <h3 id="terms" class='is-size-small'>
                                Terms of use
                            </h3>
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>
 
 
---
 
## Technology
 
The following sections contain technology specific information for technologies that underpin the CPC environment:
 
---
 
<div>
    <div class="grid is-fibonacci">
        <div class="grid-item">
            <div class="columns is-mobile is-gapless has-box-shadow-heavy has-border-radius-large has-overflow-hidden is-relative"
                data-bi-name="card">
                <div class="column is-4">
                    <div class="is-flex has-flex-align-items-center has-flex-justify-content-center is-full-height"
                        style="background-color: #00518F;">
                        <span aria-hidden="true">
                            <i class="fas fa-terminal fa-2x"></i>
                        </span>
                    </div>
                </div>
                <div class="column is-8 has-body-background">
                    <div class="has-padding-medium">
                        <a href="/appservices/" class='is-block stretched-link' data-linktype='absolute-path'>
                            <h3 id="appServices" class='is-size-small'>
                                App Services
                            </h3>
                        </a>
                        <p class="is-size-small has-line-height-reset has-text-subtle has-margin-top-small">
                            App Service Docs.
                        </p>
                    </div>
                </div>
            </div>
        </div>
        <div class="grid-item">
            <div class="columns is-mobile is-gapless has-box-shadow-heavy has-border-radius-large has-overflow-hidden is-relative"
                data-bi-name="card">
                <div class="column is-4">
                    <div class="is-flex has-flex-align-items-center has-flex-justify-content-center is-full-height"
                        style="background-color: #00518F;">
                        <span aria-hidden="true">
                            <i class="fas fa-cogs fa-2x"></i>
                        </span>
                    </div>
                </div>
                <div class="column is-8 has-body-background">
                    <div class="has-padding-medium">
                        <a href="/automation/" class='is-block stretched-link' data-linktype='absolute-path'>
                            <h3 id="automation" class='is-size-small'>
                                Automation
                            </h3>
                        </a>
                        <p class="is-size-small has-line-height-reset has-text-subtle has-margin-top-small">
                            Automation Docs.
                        </p>
                    </div>
                </div>
            </div>
        </div>
        <div class="grid-item">
            <div class="columns is-mobile is-gapless has-box-shadow-heavy has-border-radius-large has-overflow-hidden is-relative"
                data-bi-name="card">
                <div class="column is-4">
                    <div class="is-flex has-flex-align-items-center has-flex-justify-content-center is-full-height"
                        style="background-color: #00518F;">
                        <span aria-hidden="true">
                            <i class="fas fa-pound-sign fa-2x"></i>
                        </span>
                    </div>
                </div>
                <div class="column is-8 has-body-background">
                    <div class="has-padding-medium">
                        <a href="/costAndBilling/" class='is-block stretched-link' data-linktype='absolute-path'>
                            <h3 id="costAndBilling" class='is-size-small'>
                                Costs And Billing
                            </h3>
                        </a>
                        <p class="is-size-small has-line-height-reset has-text-subtle has-margin-top-small">
                            Costs And Billing Docs.
                        </p>
                    </div>
                </div>
            </div>
        </div>
        <div class="grid-item">
            <div class="columns is-mobile is-gapless has-box-shadow-heavy has-border-radius-large has-overflow-hidden is-relative"
                data-bi-name="card">
                <div class="column is-4">
                    <div class="is-flex has-flex-align-items-center has-flex-justify-content-center is-full-height"
                        style="background-color: #0065B3;">
                        <span aria-hidden="true">
                            <i class="fas fa-desktop fa-2x"></i>
                        </span>
                    </div>
                </div>
                <div class="column is-8 has-body-background">
                    <div class="has-padding-medium">
                        <a href="/compute/" class='is-block stretched-link' data-linktype='absolute-path'>
                            <h3 id="compute" class='is-size-small'>
                                Compute
                            </h3>
                        </a>
                        <p class="is-size-small has-line-height-reset has-text-subtle has-margin-top-small">
                            Compute Docs.
                        </p>
                    </div>
                </div>
            </div>
        </div>
                <div class="grid-item">
            <div class="columns is-mobile is-gapless has-box-shadow-heavy has-border-radius-large has-overflow-hidden is-relative"
                data-bi-name="card">
                <div class="column is-4">
                    <div class="is-flex has-flex-align-items-center has-flex-justify-content-center is-full-height"
                        style="background-color: #0065B3;">
                        <span aria-hidden="true">
                            <i class="fas fa-code-branch fa-2x"></i>
                        </span>
                    </div>
                </div>
                <div class="column is-8 has-body-background">
                    <div class="has-padding-medium">
                        <a href="/devops/" class='is-block stretched-link' data-linktype='absolute-path'>
                            <h3 id="devops" class='is-size-small'>
                                DevOps
                            </h3>
                        </a>
                        <p class="is-size-small has-line-height-reset has-text-subtle has-margin-top-small">
                            DevOps Docs.
                        </p>
                    </div>
                </div>
            </div>
        </div>
        <div class="grid-item">
            <div class="columns is-mobile is-gapless has-box-shadow-heavy has-border-radius-large has-overflow-hidden is-relative"
                data-bi-name="card">
                <div class="column is-4">
                    <div class="is-flex has-flex-align-items-center has-flex-justify-content-center is-full-height"
                        style="background-color: #0065B3;">
                        <span aria-hidden="true">
                            <i class="fas fa-balance-scale fa-2x"></i>
                        </span>
                    </div>
                </div>
                <div class="column is-8 has-body-background">
                    <div class="has-padding-medium">
                        <a href="/governance/" class='is-block stretched-link' data-linktype='absolute-path'>
                            <h3 id="governance" class='is-size-small'>
                                Governance
                            </h3>
                        </a>
                        <p class="is-size-small has-line-height-reset has-text-subtle has-margin-top-small">
                            Governance Docs.
                        </p>
                    </div>
                </div>
            </div>
        </div>
        <div class="grid-item">
            <div class="columns is-mobile is-gapless has-box-shadow-heavy has-border-radius-large has-overflow-hidden is-relative"
                data-bi-name="card">
                <div class="column is-4">
                    <div class="is-flex has-flex-align-items-center has-flex-justify-content-center is-full-height"
                        style="background-color: #0065B3;">
                        <span aria-hidden="true">
                            <i class="fas fa-id-card fa-2x"></i>
                        </span>
                    </div>
                </div>
                <div class="column is-8 has-body-background">
                    <div class="has-padding-medium">
                        <a href="/identity/" class='is-block stretched-link' data-linktype='absolute-path'>
                            <h3 id="identity" class='is-size-small'>
                                Identity
                            </h3>
                        </a>
                        <p class="is-size-small has-line-height-reset has-text-subtle has-margin-top-small">
                            Identity Docs.
                        </p>
                    </div>
                </div>
            </div>
        </div>
        <div class="grid-item">
            <div class="columns is-mobile is-gapless has-box-shadow-heavy has-border-radius-large has-overflow-hidden is-relative"
                data-bi-name="card">
                <div class="column is-4">
                    <div class="is-flex has-flex-align-items-center has-flex-justify-content-center is-full-height"
                        style="background-color: #0065B3;">
                        <span aria-hidden="true">
                            <i class="fas fa-search fa-2x"></i>
                        </span>
                    </div>
                </div>
                <div class="column is-8 has-body-background">
                    <div class="has-padding-medium">
                        <a href="/monitoring/" class='is-block stretched-link' data-linktype='absolute-path'>
                            <h3 id="monitoring" class='is-size-small'>
                                Monitoring
                            </h3>
                        </a>
                        <p class="is-size-small has-line-height-reset has-text-subtle has-margin-top-small">
                           Monitoring Docs.
                        </p>
                    </div>
                </div>
            </div>
        </div>
        <div class="grid-item">
            <div class="columns is-mobile is-gapless has-box-shadow-heavy has-border-radius-large has-overflow-hidden is-relative"
                data-bi-name="card">
                <div class="column is-4">
                    <div class="is-flex has-flex-align-items-center has-flex-justify-content-center is-full-height"
                        style="background-color: #0065B3;">
                        <span aria-hidden="true">
                            <i class="fas fa-network-wired fa-2x"></i>
                        </span>
                    </div>
                </div>
                <div class="column is-8 has-body-background">
                    <div class="has-padding-medium">
                        <a href="/networks/" class='is-block stretched-link' data-linktype='absolute-path'>
                            <h3 id="networking" class='is-size-small'>
                                Networking
                            </h3>
                        </a>
                        <p class="is-size-small has-line-height-reset has-text-subtle has-margin-top-small">
                            Networking Docs.
                        </p>
                    </div>
                </div>
            </div>
        </div>
                <div class="grid-item">
            <div class="columns is-mobile is-gapless has-box-shadow-heavy has-border-radius-large has-overflow-hidden is-relative"
                data-bi-name="card">
                <div class="column is-4">
                    <div class="is-flex has-flex-align-items-center has-flex-justify-content-center is-full-height"
                        style="background-color: #00518F;">
                        <span aria-hidden="true">
                            <i class="fas fa-lock fa-2x"></i>
                        </span>
                    </div>
                </div>
                <div class="column is-8 has-body-background">
                    <div class="has-padding-medium">
                        <a href="/security/" class='is-block stretched-link' data-linktype='absolute-path'>
                            <h3 id="security" class='is-size-small'>
                                Security
                            </h3>
                        </a>
                        <p class="is-size-small has-line-height-reset has-text-subtle has-margin-top-small">
                            Security Docs.
                        </p>
                    </div>
                </div>
            </div>
        </div>
        <div class="grid-item">
            <div class="columns is-mobile is-gapless has-box-shadow-heavy has-border-radius-large has-overflow-hidden is-relative"
                data-bi-name="card">
                <div class="column is-4">
                    <div class="is-flex has-flex-align-items-center has-flex-justify-content-center is-full-height"
                        style="background-color: #0065B3;">
                        <span aria-hidden="true">
                            <i class="fas fa-server fa-2x"></i>
                        </span>
                    </div>
                </div>
                <div class="column is-8 has-body-background">
                    <div class="has-padding-medium">
                        <a href="/storage/" class='is-block stretched-link' data-linktype='absolute-path'>
                            <h3 id="storage" class='is-size-small'>
                                Storage
                            </h3>
                        </a>
                        <p class="is-size-small has-line-height-reset has-text-subtle has-margin-top-small">
                            Storage Docs.
                        </p>
                    </div>
                </div>
            </div>
        </div>
     </div>
</div>
 
## Other
 
The following sections contains other relevant information relating to the CPC environment:
 
---
<div>
    <div class="grid is-fibonacci">
        <div class="grid-item">
            <div class="columns is-mobile is-gapless has-box-shadow-heavy has-border-radius-large has-overflow-hidden is-relative"
                data-bi-name="card">
                <div class="column is-4">
                    <div class="is-flex has-flex-align-items-center has-flex-justify-content-center is-full-height"
                        style="background-color: #68707D;">
                        <span aria-hidden="true">
                            <i class="fas fa-archive fa-2x"></i>
                        </span>
                    </div>
                </div>
                <div class="column is-8 has-body-background">
                    <div class="has-padding-medium">
                        <a href="/archive/" class='is-block stretched-link' data-linktype='absolute-path'>
                            <h3 id="archive" class='is-size-small'>
                                Archive
                            </h3>
                        </a>
                        <p class="is-size-small has-line-height-reset has-text-subtle has-margin-top-small">
                            Archived Docs.
                        </p>
                    </div>
                </div>
            </div>
        </div>
        <div class="grid-item">
            <div class="columns is-mobile is-gapless has-box-shadow-heavy has-border-radius-large has-overflow-hidden is-relative"
                data-bi-name="card">
                <div class="column is-4">
                    <div class="is-flex has-flex-align-items-center has-flex-justify-content-center is-full-height"
                        style="background-color: #68707D;">
                        <span aria-hidden="true">
                            <i class="fas fa-paper-plane fa-2x"></i>
                        </span>
                    </div>
                </div>
                <div class="column is-8 has-body-background">
                    <div class="has-padding-medium">
                        <a href="mailto:monty.lidher@education.gov.uk" class="is-block stretched-link" data-linktype="absolute-path">
                            <h3 id="contact" class='is-size-small'>
                                Contact
                            </h3>
                        </a>
                        <p class="is-size-small has-line-height-reset has-text-subtle has-margin-top-small">
                            Get in touch with the CPC Team.
                        </p>
                    </div>
                </div>
            </div>
        </div>