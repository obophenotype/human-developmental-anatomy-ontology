all: aeo.owl ehdaa2.owl

aeo.owl: aeo-edit.obo
	ontology-release-runner --allow-overwrite --reasoner hermit --outdir . $<

ehdaa2.owl: ehdaa2-edit.obo
	ontology-release-runner --allow-overwrite --reasoner hermit --outdir . $<
