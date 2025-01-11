# Selection Sort

## LuaU (Example):
```luau
local function selectionSort(t: {number}, descending: boolean): {number}
	local t0 = {}
	for i = 1, #t do
		local min = if descending then math.min(unpack(t)) else math.max(unpack(t))
		t0[i] = min
		table.remove(t, table.find(t, min))
	end
	return t0
end

local newT = selectionSort({-9, 0, 1, -7, 2, 9, 9000}, true)

print(newT) -- {-9, -7, 0, 1, 2, 9, 9000}
```
