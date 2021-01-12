<script>
    export let couple;
    export let famText;
    export let people;
    export let names;

    import { Col, Container, Row } from 'sveltestrap';
    import {
    Button,
    Card,
    CardBody,
    CardFooter,
    CardHeader,
    CardSubtitle,
    CardText,
    CardTitle
  } from 'sveltestrap';
</script>

<style>
    h5,h6{
        text-align: center;
        margin: 0;
        padding: 0;
    }

    .bioP {
    margin-bottom: .5rem;
    font-family: Georgia, Cambria, "Times New Roman", Times, serif;
    text-indent: 0;
    font-size: 1rem;
    }

    .personName {
        font-weight: bold;
    }

    .treeLink {
        text-align: center;
    }

</style>

<Container>

    <!-- This component displays a bootstrap card for a single couple/family -->
    <Card class="mb-5 shadow">

        <!-- The card header: names of the couple, whose ancestor they are, link for showing their tree -->
        <CardHeader class="py-1">
            <h5>{couple.theirNames}</h5>
            <h6>{couple.theirRelationship}</h6>
            <p class="treeLink">show family tree</p>
      </CardHeader>

      <CardBody>

        <CardText>

            <Row>

                {#each people as person}

                <Col xs="6">

                    <Card class="p-2 mb-2 border-light shadow">

                        <Row>
                            <Col xs="3">
                                <img class="float-left" src="{person.personPic}" alt="personImage" width=100>
                            </Col>

                            <Col xs="9">
                                <span class="personName">{person.personName}</span><br>
                                Born {person.personBorn}<br>
                                Arrived {person.personArv}<br>
                                Died {person.personDied}<br>
                            </Col>
                        </Row>

                </Card>

                </Col>

                {/each} <!-- end of loop on all (max 2) people in this couple -->

            </Row>

            <Row>
                <Col xs="12">
                    <p  class="bioP">{famText}</p>
                </Col>
            </Row>
                  
        </CardText>

    </CardBody>

    </Card>

</Container>
