OBO= http://purl.obolibrary.org/obo

all: aeo.owl ehdaa2.owl 
## all: aeo.owl ehdaa2.owl uberon-check.txt -- https://github.com/cmungall/human-developmental-anatomy-ontology/issues/2

aeo.owl: aeo-edit.obo
	ontology-release-runner --allow-overwrite --reasoner hermit --outdir . $<
aeo.obo: aeo.owl

ehdaa2.owl: ehdaa2-edit.obo
	ontology-release-runner --allow-overwrite --reasoner hermit --outdir . $<

# Disabled until https://github.com/cmungall/human-developmental-anatomy-ontology/issues/2 fixed
uberon-check.txt: ehdaa2.owl
	owltools ehdaa2.owl $(OBO)/uberon.owl $(OBO)/uberon/bridge/uberon-bridge-to-ehdaa2.owl $(OBO)/uberon/external-disjoints.owl --merge-support-ontologies --run-reasoner -r elk -u > $@
