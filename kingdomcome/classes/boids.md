<!-- TITLE: Boids Function Reference -->

# Boids Class
## Patreon

If you want to see more resources like this, [become a Patreon supporter!](https://www.patreon.com/fireundubh) 

## Enums

Key | Value
--- | ---
FLOCK_BIRDS | 0
FLOCK_FISH | 1
FLOCK_BUGS | 2
FLOCK_CHICKENS | 3
FLOCK_FROGS | 4
FLOCK_TURTLES | 5

## Methods

### CreateFlock

No description entered

#### **Syntax**

`local result = Boids.CreateFlock(entity, nType, tParamsTable)`

#### **Parameters**

* `entity`: An entity, usually `self`
* `nType`: An enum member indicating the type of flock
* `tParamsTable`: A table of flock parameters (see `Scripts\Entities\Boids\Birds.lua` for an example)

#### **Return value**

`nil`


### EnableFlock

No description entered

#### **Syntax**

`Boids.EnableFlock(entity, bEnable)`

#### **Parameters**

* `entity`: An entity, usually `self`
* `bEnable`: A boolean indicating whether the flock is enabled or disabled

#### **Return value**

`nil`


### OnBoidHit

No description entered

#### **Syntax**

`Boids.OnBoidHit(boidEntity, entity, hit)`

#### **Parameters**

* `boidEntity`: A flock entity
* `entity`:  An entity, usually `self`
* `hit`: A boolean indicating whether the boid was hit

#### **Return value**

`nil`


### SetAttractionPoint

No description entered

#### **Syntax**

`Boids.SetAttractionPoint(entity, point)`

#### **Parameters**

* `entity`: An entity, usually `self`
* `point`: A Vec3 table (e.g., `{x = 0, y = 0, z = 0}`)

#### **Return value**

`nil`


### SetFlockParams

No description entered

#### **Syntax**

`Boids.SetFlockParams(entity, tParamsTable)`

#### **Parameters**

* `entity`: An entity, usually `self`
* `tParamsTable`: A table of flock parameters (see `Scripts\Entities\Boids\Birds.lua` for an example)

#### **Return value**

`nil`


### SetFlockPercentEnabled

No description entered

#### **Syntax**

`Boids.SetFlockPercentEnabled(entity, fPercentage)`

#### **Parameters**

* `entity`: An entity, usually `self`
* `fPercentage`: A number indicating the fade coefficient

#### **Return value**

`nil`

