
It's simple, straightforward, and leverages the power of extension methods to make the mapping process more readable and maintainable.

public static class TestMapper
{
	public static NeedMappingObject MapToObject(this IncomingObject incomingObject)
	{
		if (incomingObject is null) 
		{ 
			throw new ArgumentNullException(nameof(incomingObject));
		}
		var result = new NeedMappingObject
		{
			Name = incomingObject.Name,
			 Type = incomingObject.Type
		}
		return result;
	}
}