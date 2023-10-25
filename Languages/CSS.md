Everything displayed by CSS is a **box**.

## Extrinsic vs Intrinsic
Extrinsic sizing manually sets sizing of box components:
<main>
	<div>
		<p class="awesome">AWESOME</p>
	</div>
</main>
Intrinsic could be used instead:
<main>
	<div>
		<p class="awesome-int">AWESOME</p>
	</div>
</main>
> [!info]
> Using extrinsic sizing, there is a limit to how much content can be added before the content will overflow outside of the box's bounds.


## Box model
Boxes are made of areas which each do a specific job
![[Pasted image 20231025121631.png]]