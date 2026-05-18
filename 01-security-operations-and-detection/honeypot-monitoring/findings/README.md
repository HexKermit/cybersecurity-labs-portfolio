# Investigation Findings

## Summary

This investigation focused on deploying and validating a simple HTTP honeypot within a controlled lab environment.

The honeypot service was configured on port 80 using PenTBox and successfully responded to inbound browser requests with a custom warning message.

The lab demonstrated how deception-based monitoring can improve network visibility and support defensive awareness during early-stage reconnaissance activity.

---

## Key Findings

### 1. Honeypot Deployment Validation

The honeypot service was successfully configured and activated on port 80.

This confirmed:
- listener configuration functionality
- service activation
- inbound connection readiness
- basic monitoring capability

---

### 2. Browser Access Validation

A browser connection to the honeypot IP address successfully displayed the configured warning message.

This demonstrated:
- active HTTP response behavior
- reachable honeypot service exposure
- successful validation of the deception response

---

### 3. Monitoring Visibility

The honeypot configuration process demonstrated how defenders can deploy lightweight monitoring services to identify unexpected inbound access attempts.

Observed monitoring concepts included:
- service exposure awareness
- access observation
- deception-based visibility
- inbound traffic monitoring

---

### 4. Deception-Based Security Awareness

The lab reinforced how honeypots can support defensive operations by improving visibility into unexpected or suspicious access behavior directed toward monitored services.

This can improve:
- early-stage threat visibility
- suspicious access awareness
- reconnaissance observation
- defensive investigation readiness

---

## Security Impact

Unmonitored services may allow attackers to:
- identify accessible systems
- validate active hosts
- perform reconnaissance activity
- profile exposed services

Even simple honeypots can help defenders better understand unexpected network access behavior.

---

## Analyst Notes

This lab improved understanding of:
- honeypot deployment workflows
- controlled monitoring concepts
- deception-based security monitoring
- inbound traffic visibility
- defensive security awareness

The investigation also highlighted the importance of realistic defensive monitoring expectations when working with lightweight honeypot deployments in controlled environments.
