
Security Documentation
Overview

This document describes the basic security considerations applied to the Tarliam Global website during development and deployment.

The purpose was to build a functional business website while considering common web security risks and protecting users interacting with the website.

Security Considerations
HTTPS

The website is deployed over HTTPS to encrypt communication between the user's browser and the website.

Contact Form

The website uses Formspree to process contact form submissions rather than directly handling or storing submitted information on the website's frontend.

Sensitive Information

No passwords, payment information, authentication credentials, or other sensitive user information is intentionally collected or stored by the website.

Input Handling

The contact form is designed to accept basic customer enquiry information. Form processing is handled through the external form service rather than through a custom backend.

Deployment

The website is deployed using Netlify. Deployment and hosting configuration were considered as part of the project's security and reliability requirements.

Security Testing

Basic security testing and review will be performed as part of the project's development process.

Planned checks include:

HTTPS and TLS configuration
HTTP security headers
DNS configuration
Open ports and exposed services
Basic web application security checks
Form behaviour and input handling
Common configuration issues

Any findings will be documented along with recommended improvements.

Limitations

This project is a business website and was not designed as a security-critical application.

This documentation does not claim that the website is completely secure. Security testing is intended to identify common issues and improve the overall security posture of the website.
