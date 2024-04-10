
public static class TestMapper
{
	public static NeedMappingObject MapToObject(this IncomingObject incomingObject)
	{
		var result = new NeedMappingObject
		{
			Name = incomingObject.Name,
			 Type = incomingObject.Typpe
		}
		return result;
	}
}