---
title: "OpenID Connect standard claims registration for CBOR Web Tokens"
abbrev: "OIDC standard claims for CWT"
category: info

docname: draft-maldant-spice-oidc-cwt-latest
submissiontype: IETF  # also: "independent", "editorial", "IAB", or "IRTF"
number:
date:
consensus: true
v: 3
area: "Security"
workgroup: "Secure Patterns for Internet CrEdentials"
keyword:
 - openid connect
 - oidc
 - standard claims
venue:
  group: "Secure Patterns for Internet CrEdentials"
  type: "Working Group"
  mail: "spice@ietf.org"
  arch: "https://mailarchive.ietf.org/arch/browse/spice/"
  github: "beltram/rfc-spice-oidc-cwt"
  latest: "https://beltram.github.io/rfc-spice-oidc-cwt/draft-maldant-spice-oidc-cwt.html"

author:
 - fullname: "Beltram Maldant"
   organization: SimpleLogin
   email: "beltram.ietf@pm.me"

normative:
    OIDCCore:
        target: https://openid.net/specs/openid-connect-core-1_0.html
        title: "OpenID Connect Core 1.0 incorporating errata set 2"
        date: 2023-12-15
        author:
            - name: Nat Sakimura
            - name: John Bradley
            - name: Michael B. Jones
            - name: Breno de Medeiros
            - name: Chuck Mortimore
    IANAtimezones:
        target: https://www.iana.org/time-zones
        title: "IANA time zones"
    ISO8601‑1:
        target: https://www.iso.org/standard/81801.html
        title: "ISO8601‑1"

informative:

--- abstract

This document registers OpenId Connect standards claims already used in JSON Web Tokens for CBOR Web Tokens.


--- middle

# Introduction

OpenId Connect {{OIDCCore}} is an authentication standard including standard claims already in use for JSON Web Tokens (JWT) {{?RFC7519}}. CBOR Web Tokens (CWT) {{!RFC8392}} have a claims registry, but do not include most of these claims. This draft aims at unifying use of OIDC claims in JWTs and CWTs.

# Conventions and Definitions

{::boilerplate bcp14-tagged}


# Security Considerations

This document registers existing OpenID Connect standard claims already used in JSON Web Tokens {{?RFC7519}} for use in CBOR Web Tokens {{!RFC8392}} without changing their semantics. The Security and Privacy Considerations respectively of Sections 16 and 17 of {{OIDCCore}} also apply.

# IANA Considerations

## name

- Claim Name: name
- Claim Description: End-User's full name in displayable form including all name parts, possibly including titles and suffixes, ordered according to the End-User's locale and preferences.
- JWT Claim Name: name
- Claim Key: TBD (requested assignment 170)
- Claim Value Type(s): text string
- Change Controller: IESG
- Specification Document(s): Section 5.1 of {{OIDCCore}}

## given_name

- Claim Name: given_name
- Claim Description: Given name(s) or first name(s) of the End-User.
- JWT Claim Name: given_name
- Claim Key: TBD (requested assignment 171)
- Claim Value Type(s): text string
- Change Controller: IESG
- Specification Document(s): Section 5.1 of {{OIDCCore}}

## family_name

- Claim Name: family_name
- Claim Description: Surname(s) or last name(s) of the End-User.
- JWT Claim Name: family_name
- Claim Key: TBD (requested assignment 172)
- Claim Value Type(s): text string
- Change Controller: IESG
- Specification Document(s): Section 5.1 of {{OIDCCore}}

## middle_name

- Claim Name: middle_name
- Claim Description: Middle name(s) of the End-User.
- JWT Claim Name: middle_name
- Claim Key: TBD (requested assignment 173)
- Claim Value Type(s): text string
- Change Controller: IESG
- Specification Document(s): Section 5.1 of {{OIDCCore}}

## nickname

- Claim Name: nickname
- Claim Description: Casual name of the End-User that may or may not be the same as the given_name.
- JWT Claim Name: nickname
- Claim Key: TBD (requested assignment 174)
- Claim Value Type(s): text string
- Change Controller: IESG
- Specification Document(s): Section 5.1 of {{OIDCCore}}

## preferred_username

- Claim Name: preferred_username
- Claim Description: Shorthand name by which the End-User wishes to be referred to at the Resource Server.
- JWT Claim Name: preferred_username
- Claim Key: TBD (requested assignment 175)
- Claim Value Type(s): text string
- Change Controller: IESG
- Specification Document(s): Section 5.1 of {{OIDCCore}}

## profile

- Claim Name: profile
- Claim Description: URL of the End-User's profile page.
- JWT Claim Name: profile
- Claim Key: TBD (requested assignment 176)
- Claim Value Type(s): text string
- Change Controller: IESG
- Specification Document(s): Section 5.1 of {{OIDCCore}}

## picture

- Claim Name: picture
- Claim Description: URL of the End-User's profile picture. This URL MUST refer to an image file, rather than to a Web page containing an image.
- JWT Claim Name: picture
- Claim Key: TBD (requested assignment 177)
- Claim Value Type(s): text string
- Change Controller: IESG
- Specification Document(s): Section 5.1 of {{OIDCCore}}

## website

- Claim Name: website
- Claim Description: URL of the End-User's Web page or blog.
- JWT Claim Name: website
- Claim Key: TBD (requested assignment 178)
- Claim Value Type(s): text string
- Change Controller: IESG
- Specification Document(s): Section 5.1 of {{OIDCCore}}

## email

- Claim Name: email
- Claim Description: End-User's preferred e-mail address.
- JWT Claim Name: email
- Claim Key: TBD (requested assignment 179)
- Claim Value Type(s): text string
- Change Controller: IESG
- Specification Document(s): Section 5.1 of {{OIDCCore}}

## email_verified

- Claim Name: email_verified
- Claim Description: True if the End-User's e-mail address has been verified; otherwise false.
- JWT Claim Name: email_verified
- Claim Key: TBD (requested assignment 180)
- Claim Value Type(s): text string
- Change Controller: IESG
- Specification Document(s): Section 5.1 of {{OIDCCore}}

## gender

- Claim Name: gender
- Claim Description: End-User's defined gender.
- JWT Claim Name: gender
- Claim Key: TBD (requested assignment 181)
- Claim Value Type(s): text string
- Change Controller: IESG
- Specification Document(s): Section 5.1 of {{OIDCCore}}

## birthdate

- Claim Name: birthdate
- Claim Description: End-User's birthday, represented as an [ISO8601‑1] YYYY-MM-DD format.
- JWT Claim Name: birthdate
- Claim Key: TBD (requested assignment 182)
- Claim Value Type(s): text string
- Change Controller: IESG
- Specification Document(s): Section 5.1 of {{OIDCCore}}

## zoneinfo

- Claim Name: zoneinfo
- Claim Description: String from IANA Time Zone Database {{IANAtimezones}} representing the End-User's time zone.
- JWT Claim Name: zoneinfo
- Claim Key: TBD (requested assignment 183)
- Claim Value Type(s): text string
- Change Controller: IESG
- Specification Document(s): Section 5.1 of {{OIDCCore}}

## locale

- Claim Name: locale
- Claim Description: End-User's locale, represented as a BCP47 {{!RFC5646}} language tag.
- JWT Claim Name: locale
- Claim Key: TBD (requested assignment 184)
- Claim Value Type(s): text string
- Change Controller: IESG
- Specification Document(s): Section 5.1 of {{OIDCCore}}

## phone_number

- Claim Name: phone_number
- Claim Description: End-User's preferred telephone number.
- JWT Claim Name: phone_number
- Claim Key: TBD (requested assignment 185)
- Claim Value Type(s): text string
- Change Controller: IESG
- Specification Document(s): Section 5.1 of {{OIDCCore}}

## phone_number_verified

- Claim Name: phone_number_verified
- Claim Description:  True if the End-User's phone number has been verified; otherwise false.
- JWT Claim Name: phone_number_verified
- Claim Key: TBD (requested assignment 186)
- Claim Value Type(s): text string
- Change Controller: IESG
- Specification Document(s): Section 5.1 of {{OIDCCore}}

## address

- Claim Name: address
- Claim Description: End-User's preferred postal address.
- JWT Claim Name: address
- Claim Key: TBD (requested assignment 187)
- Claim Value Type(s): text string (the content is a JSON array)
- Change Controller: IESG
- Specification Document(s): Section 5.1 of {{OIDCCore}}

## updated_at

- Claim Name: updated_at
- Claim Description: Time the End-User's information was last updated. Its value is a number representing the number of seconds from 1970-01-01T00:00:00Z as measured in UTC until the date/time.
- JWT Claim Name: updated_at
- Claim Key: TBD (requested assignment 188)
- Claim Value Type(s): uint
- Change Controller: IESG
- Specification Document(s): Section 5.1 of {{OIDCCore}}

--- back

# CDDL Schema {#cddl}

~~~~~~~~~~
{::include ./oidc-claims.cddl}
~~~~~~~~~~
{: #cddl-schema title="A CDDL description of each claim"}

