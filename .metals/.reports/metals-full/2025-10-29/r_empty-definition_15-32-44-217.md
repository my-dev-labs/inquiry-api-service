error id: file://<WORKSPACE>/assessment-api/assessment-service/app/modules/AssessmentModule.scala:scala/Predef.classOf().
file://<WORKSPACE>/assessment-api/assessment-service/app/modules/AssessmentModule.scala
empty definition using pc, found symbol in pc: scala/Predef.classOf().
empty definition using semanticdb
empty definition using fallback
non-local guesses:
	 -classOf.
	 -classOf#
	 -classOf().
	 -scala/Predef.classOf.
	 -scala/Predef.classOf#
	 -scala/Predef.classOf().
offset: 575
uri: file://<WORKSPACE>/assessment-api/assessment-service/app/modules/AssessmentModule.scala
text:
```scala
package modules

import com.google.inject.AbstractModule
import play.libs.pekko.PekkoGuiceSupport
import utils.ActorNames
import org.sunbird.actors.{HealthActor, ItemSetActor, QuestionActor, QuestionSetActor}
import org.sunbird.v5.actors.{QuestionActor => QuestionV5Actor, QuestionSetActor => QuestionSetV5Actor}

class AssessmentModule extends AbstractModule with PekkoGuiceSupport {

    override def configure() = {
        bindActor(classOf[HealthActor], ActorNames.HEALTH_ACTOR)
        bindActor(classOf[ItemSetActor], ActorNames.ITEM_SET_ACTOR)
        bindActor(class@@Of[QuestionActor], ActorNames.QUESTION_ACTOR)
        bindActor(classOf[QuestionSetActor], ActorNames.QUESTION_SET_ACTOR)
        bindActor(classOf[QuestionV5Actor], ActorNames.QUESTION_V5_ACTOR)
        bindActor(classOf[QuestionSetV5Actor], ActorNames.QUESTION_SET_V5_ACTOR)
        println("Initialized application actors for assessment-service")
    }
}

```


#### Short summary: 

empty definition using pc, found symbol in pc: scala/Predef.classOf().