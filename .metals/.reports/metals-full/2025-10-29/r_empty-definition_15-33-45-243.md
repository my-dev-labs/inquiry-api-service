error id: file://<WORKSPACE>/assessment-api/assessment-actors/src/main/scala/org/sunbird/actors/HealthActor.scala:`<none>`.
file://<WORKSPACE>/assessment-api/assessment-actors/src/main/scala/org/sunbird/actors/HealthActor.scala
empty definition using pc, found symbol in pc: `<none>`.
empty definition using semanticdb
empty definition using fallback
non-local guesses:
	 -org/sunbird/common/dto/Request.
	 -org/sunbird/common/dto/Request#
	 -org/sunbird/common/dto/Request().
	 -Request.
	 -Request#
	 -Request().
	 -scala/Predef.Request.
	 -scala/Predef.Request#
	 -scala/Predef.Request().
offset: 131
uri: file://<WORKSPACE>/assessment-api/assessment-actors/src/main/scala/org/sunbird/actors/HealthActor.scala
text:
```scala
package org.sunbird.actors

import javax.inject.Inject
import org.sunbird.actor.core.BaseActor
import org.sunbird.common.dto.{Reque@@st, Response}
import org.sunbird.graph.OntologyEngineContext
import org.sunbird.graph.health.HealthCheckManager

import scala.concurrent.{ExecutionContext, Future}


class HealthActor @Inject() (implicit oec: OntologyEngineContext) extends BaseActor {

    implicit val ec: ExecutionContext = getContext().dispatcher

    @throws[Throwable]
    override def onReceive(request: Request): Future[Response] = {
        HealthCheckManager.checkAllSystemHealth()
    }
}

```


#### Short summary: 

empty definition using pc, found symbol in pc: `<none>`.