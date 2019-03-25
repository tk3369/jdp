## Cost of Splatting

Be careful with the performance impact.  It gets progressively more expensive very quickly.

```julia
julia> r = [DataFrame(rand(10,i)) for i in (2, 5, 10, 20, 40, 80, 160)];

julia> for df in r
         b1 = @benchmark promote_type(eltypes($df)...)
         b2 = @benchmark reduce(promote_type, eltypes($df))
         @show b1 b2 judge(minimum(b1), minimum(b2))
       end
b1 = Trial(1.557 μs)
b2 = Trial(1.728 μs)
judge(minimum(b1), minimum(b2)) = TrialJudgement(-9.87% => improvement)
b1 = Trial(9.547 μs)
b2 = Trial(3.653 μs)
judge(minimum(b1), minimum(b2)) = TrialJudgement(+161.35% => regression)
b1 = Trial(33.208 μs)
b2 = Trial(6.812 μs)
judge(minimum(b1), minimum(b2)) = TrialJudgement(+387.51% => regression)
b1 = Trial(105.270 μs)
b2 = Trial(13.250 μs)
judge(minimum(b1), minimum(b2)) = TrialJudgement(+694.49% => regression)
b1 = Trial(347.071 μs)
b2 = Trial(25.844 μs)
judge(minimum(b1), minimum(b2)) = TrialJudgement(+1242.95% => regression)
b1 = Trial(1.228 ms)
b2 = Trial(51.259 μs)
judge(minimum(b1), minimum(b2)) = TrialJudgement(+2294.98% => regression)
b1 = Trial(4.590 ms)
b2 = Trial(101.875 μs)
judge(minimum(b1), minimum(b2)) = TrialJudgement(+4405.36% => regression)
```