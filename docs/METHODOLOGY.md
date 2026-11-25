# Research Methodology

## Objective

Measure observable data-handling behaviour across AI inference paths using unique synthetic canaries and controlled callbacks.

## Experiment lifecycle

1. **Define scope:** identify client, route, provider, endpoint, test window and authorisation basis.
2. **Create synthetic canaries:** generate unique opaque markers and inert credential-shaped strings that cannot authenticate.
3. **Instrument locally:** record minimal request metadata and apply local secret-pattern checks before egress.
4. **Send controlled requests:** use documented test prompts and provider-approved endpoints.
5. **Observe callbacks:** collect timestamp, canary ID, callback source metadata and request correlation where available.
6. **Correlate:** compare callbacks with experiment windows and route records.
7. **Report cautiously:** classify observations without asserting intent or compromise beyond the evidence.

## Observation classifications

- `no_callback_observed`: no callback seen within the declared observation window.
- `canary_callback_observed`: controlled canary endpoint received a request.
- `credential_validation_attempt_observed`: a sandbox credential was tested against an isolated test account.
- `confirmed_unauthorised_action`: a prohibited action was observed in the sandbox audit trail.
- `inconclusive`: evidence is insufficient or correlation is ambiguous.

## Limitations

A missing callback does not prove non-retention or non-access. A callback does not identify the actor or prove malicious intent. IP geolocation is approximate. Provider routing may change. ZDR claims cannot be conclusively verified solely through external canary experiments.
