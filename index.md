---
title: Nostr
layout: default
nav_order: 1
---

<style>
  .nostr-page {
    max-width: 920px;
    line-height: 1.7;
    font-family: Georgia, "Times New Roman", Times, serif;
    color: #000;
  }

  .nostr-page .eyebrow {
    display: inline-block;
    margin-bottom: 14px;
    padding: 6px 10px;
    border-radius: 999px;
    background: #f8f9fa;
    color: #202122;
    font-size: 0.88rem;
    font-weight: 600;
    letter-spacing: 0.01em;
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Inter, Arial, sans-serif;
  }

  .nostr-page h1 {
    margin: 0 0 14px;
    font-size: clamp(2.2rem, 4vw, 3.2rem);
    line-height: 1.12;
    letter-spacing: -0.02em;
    font-family: Georgia, "Times New Roman", Times, serif;
    font-weight: 700;
    color: #000;
  }

  .nostr-page h2 {
    margin-top: 36px;
    margin-bottom: 12px;
    font-size: 1.34rem;
    line-height: 1.28;
    letter-spacing: 0;
    font-family: Georgia, "Times New Roman", Times, serif;
    font-weight: 700;
    color: #000;
  }

  .nostr-page p {
    margin: 0 0 16px;
    font-size: 1.08rem;
    color: #000;
  }

  .nostr-page .lead {
    max-width: 64ch;
    font-size: 1.16rem;
    color: #000;
  }

  .nostr-page .hero {
    overflow: hidden;
  }

  .nostr-page .profile-image {
    float: right;
    width: min(30vw, 224px);
    max-width: 224px;
    min-width: 148px;
    aspect-ratio: 1 / 1;
    object-fit: cover;
    border-radius: 0;
    margin: 4px 0 20px 28px;
    border: 1px solid #d8e0eb;
    box-shadow: 0 16px 34px rgba(15, 23, 42, 0.14);
    background: rgba(127, 127, 127, 0.12);
  }

  .nostr-page .inline-image {
    float: left;
    width: min(30vw, 224px);
    max-width: 224px;
    min-width: 148px;
    aspect-ratio: 1 / 1;
    object-fit: cover;
    border-radius: 0;
    margin: 0 52px 24px 0;
    border: 1px solid #d8e0eb;
    box-shadow: 0 16px 34px rgba(15, 23, 42, 0.14);
    background: rgba(127, 127, 127, 0.12);
  }

  .nostr-page .nip05-section {
    overflow: hidden;
    margin-top: 40px;
  }

  .nostr-page code {
    font-family: ui-monospace, SFMono-Regular, Menlo, Consolas, monospace;
    font-size: 0.95em;
    background: rgba(127, 127, 127, 0.12);
    padding: 0.16em 0.42em;
    border-radius: 6px;
  }

  .nostr-page .technical-row {
    display: flex;
    align-items: flex-start;
    gap: 24px;
    margin-top: 30px;
  }

  .nostr-page .note {
    flex: 1 1 auto;
    margin-top: 0;
    padding: 18px 18px;
    border: 1px solid #a2a9b1;
    border-radius: 0;
    background: #f8f9fa;
    color: #000;
    font-size: 1.02rem;
  }

  .nostr-page .note strong {
    color: #000;
  }

  .nostr-page .technical-side-image {
    flex: 0 0 auto;
    flex-shrink: 0;
    width: min(30vw, 224px);
    max-width: 224px;
    min-width: 148px;
    aspect-ratio: 1 / 1;
    object-fit: cover;
    border-radius: 0;
    border: 1px solid #d8e0eb;
    box-shadow: 0 16px 34px rgba(15, 23, 42, 0.14);
    background: rgba(127, 127, 127, 0.12);
  }

  @media (prefers-color-scheme: dark) {
    .nostr-page {
      color: #000;
    }

    .nostr-page .eyebrow {
      background: #f8f9fa;
      color: #202122;
    }

    .nostr-page .lead,
    .nostr-page p,
    .nostr-page h1,
    .nostr-page h2,
    .nostr-page .note,
    .nostr-page .note strong {
      color: #000;
    }

    .nostr-page .profile-image,
    .nostr-page .inline-image,
    .nostr-page .note,
    .nostr-page .technical-side-image {
      border-color: #a2a9b1;
    }

    .nostr-page .note {
      background: #f8f9fa;
    }
  }

  @media (max-width: 700px) {
    .nostr-page .profile-image,
    .nostr-page .inline-image {
      float: none;
      display: block;
      width: min(64vw, 220px);
      margin: 0 auto 20px;
    }

    .nostr-page .technical-row {
      display: block;
    }

    .nostr-page .technical-side-image {
      display: block;
      width: min(64vw, 220px);
      margin: 18px auto 0;
    }
  }
</style>

<div class="nostr-page">
  <article class="hero">
    <img src="/img01.png" alt="Profile image" class="profile-image">

    <div class="eyebrow">Personal identity page</div>
    <h1>Nostr Identity Verification</h1>
    <p class="lead">
      This is a small personal page I use to connect a public web domain to my Nostr identity. Its main purpose is simple: to provide a stable, public reference point for NIP-05 verification.
    </p>

    <h2>About this page</h2>
    <p>
      I maintain this GitHub Pages site as a lightweight personal homepage and as a technical identity page for Nostr. I wanted a public place that is easy to manage, easy to keep online, and suitable for hosting the verification file that Nostr clients can check automatically.
    </p>
    <p>
      In practice, the most important file on this site is <code>/.well-known/nostr.json</code>. That file allows a Nostr client to query this domain and confirm that this domain is intentionally associated with a particular Nostr public key.
    </p>

    <h2>What is Nostr?</h2>
    <p>
      Nostr is an open, decentralized protocol for social communication. Rather than depending on a single platform to own user accounts and identities, Nostr uses public and private key cryptography. A user proves ownership of an identity by controlling the corresponding private key and by signing events with it.
    </p>
    <p>
      One of the most interesting features of Nostr is that identity and communication are not tied to one company or one website. Different clients can read and publish the same kind of data, and different relays can carry that data. This gives users a higher degree of portability than is common on conventional social platforms.
    </p>
    <p>
      At the same time, decentralized systems benefit from clear public identity signals. A long public key is technically sufficient, but it is not especially human-friendly. That is one reason NIP-05 exists.
    </p>

    <section class="nip05-section">
      <img src="/img02.png" alt="Illustration related to NIP-05 verification" class="inline-image">
      <h2 style="margin-top: 0;">What is NIP-05?</h2>
      <p>
        NIP-05 is a Nostr standard that lets a domain publish a mapping between an internet-style identifier, such as <code>name@example.com</code>, and a Nostr public key. When a client supports NIP-05, it can look up that mapping and show that a profile is linked to the relevant domain.
      </p>
      <p>
        In everyday use, this often functions as a practical identity hint. It tells visitors that the operator of a domain has deliberately published a record pointing to a specific key. That is useful because it gives a profile a readable and publicly inspectable identity reference beyond the raw hexadecimal public key or <code>npub</code> string.
      </p>
      <p>
        It is still important to describe this carefully. NIP-05 is not a government credential, not a universal proof of legal identity, and not an endorsement by any central platform. It is better understood as a transparent domain-based statement: this domain declares that a given Nostr identifier corresponds to a given public key.
      </p>
      <p>
        In other words, NIP-05 helps make a Nostr identity easier to read and easier to verify in public. It does not replace cryptographic identity, but it adds a human-readable layer that makes a profile more understandable to other people.
      </p>
    </section>

    <h2>Why GitHub Pages?</h2>
    <p>
      I chose <code>github.io</code> because it is straightforward, public, reliable for static hosting, and more than sufficient for a page like this. I do not need a complex web application here. I only need a small, stable site that can host a short explanation and the verification file required for NIP-05.
    </p>
    <p>
      For that reason, this page is intentionally minimal. It exists first as infrastructure and second as documentation. If you arrived here from a Nostr profile, you are probably looking for confirmation that this domain is genuinely being used as part of that profile's public identity.
    </p>
    <p>
      As a personal developer site, I prefer simple tools that remain easy to understand and maintain. GitHub Pages and a small static page are enough for this purpose, and I appreciate that the result stays close to ordinary web standards. That simplicity feels appropriate for Nostr as well: an open protocol, a public key, and a small public record that anyone can verify.
    </p>

    <div class="technical-row">
      <div class="note">
        <strong>Technical note:</strong> if you are here specifically to verify my Nostr identity, the key resource on this site is <code>/.well-known/nostr.json</code>.
      </div>
      <img src="/img03.png" alt="Additional illustration" class="technical-side-image">
    </div>
  </article>
</div>
