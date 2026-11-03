# Bounded agent workflow

Example: produce a report from an authorized source. Resolve question and source scope, retrieve evidence, validate coverage, generate the draft, verify claims against evidence and return the verified artifact. When evidence is insufficient, return its known scope and the missing input. A retry resumes the failed step with validated state.

Record run ID, workflow version, state, actor, evidence handles, action receipts and stop reason. Keep credentials and private payloads outside routine traces. A safe terminal partial result includes what completed, what remains and the next permitted action.

Exercise correct tool selection, schema rejection before execution, missing and conflicting evidence, denied scope, transient failure, an ambiguous write result and budget exhaustion where relevant. Compare repeated runs on identical fixtures when claiming an improvement. Count failed and skipped cases separately.
