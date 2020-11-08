---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiSchema.md
ms.openlocfilehash: 837494b8f042d3ea788eda69d47845b02859c805
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260399"
---
# <span data-ttu-id="9aee9-101">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="9aee9-101">Get-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="9aee9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9aee9-102">SYNOPSIS</span></span>
<span data-ttu-id="9aee9-103">Få information om API-schemat</span><span class="sxs-lookup"><span data-stu-id="9aee9-103">Get the details of the API Schema</span></span>

## <span data-ttu-id="9aee9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9aee9-104">SYNTAX</span></span>

### <span data-ttu-id="9aee9-105">ContextParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="9aee9-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9aee9-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9aee9-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiSchema -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9aee9-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9aee9-107">DESCRIPTION</span></span>
<span data-ttu-id="9aee9-108">Cmdleten **Get-AzApiManagementApiSchema** hämtar information om API-schemat</span><span class="sxs-lookup"><span data-stu-id="9aee9-108">The **Get-AzApiManagementApiSchema** cmdlet gets the details of the API Schema</span></span>

## <span data-ttu-id="9aee9-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9aee9-109">EXAMPLES</span></span>

### <span data-ttu-id="9aee9-110">Exempel 1: få information om allt API-schema för ett API</span><span class="sxs-lookup"><span data-stu-id="9aee9-110">Example 1: Get the details of all the Api Schema of an Api</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/resourceGroupName/providers/Microsoft.ApiManagement/service/sdktestapim4163
PS D:\github\azure-powershell> Get-AzApiManagementApiSchema -Context $context -ApiId wsdlapitest

SchemaId           : 2a03e1b4-1826-4e59-b372-4711f575db28
Api Id             : wsdlapitest
Schema ContentType : xsdschema
Schema Document    : <s:schema elementFormDefault="qualified"....

SchemaId           : b6e5497d-f65a-4851-9f5b-b5684cdae688
Api Id             : wsdlapitest
Schema ContentType : xsdschema
Schema Document    : <?xml version=""1.0"" encoding=""UTF-8""....
```

<span data-ttu-id="9aee9-111">Det här kommandot får alla API-scheman som är kopplade till ett API `swagger-petstore-extensive` för en viss ApiManagement kontext.</span><span class="sxs-lookup"><span data-stu-id="9aee9-111">This command gets all the API schemas associated with an Api `swagger-petstore-extensive` for particular ApiManagement Context.</span></span>

### <span data-ttu-id="9aee9-112">Exempel 2: Hämta det specifika schema som är kopplat till ett API</span><span class="sxs-lookup"><span data-stu-id="9aee9-112">Example 2: Get the specific schema associated with an Api</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/resourceGroupName/providers/Microsoft.ApiManagement/service/sdktestapim4163
PS D:\github\azure-powershell> Get-AzApiManagementApiSchema -Context $context -ApiId swagger-petstore-extensive -SchemaId 5cc9cf67e6ed3b1154e638bd

SchemaId           : 5cc9cf67e6ed3b1154e638bd
Api Id             : swagger-petstore-extensive
Schema ContentType : swaggerdefinition
Schema Document    : {
                       "definitions": {
                         "pet": {
                        ....
```

<span data-ttu-id="9aee9-113">Det här kommandot får det API-schema `5cc9cf67e6ed3b1154e638bd` som är kopplat till ett API `swagger-petstore-extensive` för en viss ApiManagement-kontext.</span><span class="sxs-lookup"><span data-stu-id="9aee9-113">This command gets the API schema `5cc9cf67e6ed3b1154e638bd` associated with an Api `swagger-petstore-extensive` for particular ApiManagement Context.</span></span>

## <span data-ttu-id="9aee9-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9aee9-114">PARAMETERS</span></span>

### <span data-ttu-id="9aee9-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="9aee9-115">-ApiId</span></span>
<span data-ttu-id="9aee9-116">API-identifierare att leta efter.</span><span class="sxs-lookup"><span data-stu-id="9aee9-116">API identifier to look for.</span></span>
<span data-ttu-id="9aee9-117">Om det här alternativet anges kommer API: t att hämtas via ID.</span><span class="sxs-lookup"><span data-stu-id="9aee9-117">If specified will try to get the API by the Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9aee9-118">-Kontext</span><span class="sxs-lookup"><span data-stu-id="9aee9-118">-Context</span></span>
<span data-ttu-id="9aee9-119">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="9aee9-119">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="9aee9-120">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="9aee9-120">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9aee9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9aee9-121">-DefaultProfile</span></span>
<span data-ttu-id="9aee9-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9aee9-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9aee9-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9aee9-123">-ResourceId</span></span>
<span data-ttu-id="9aee9-124">Arm-resurs-ID för ett API-schema.</span><span class="sxs-lookup"><span data-stu-id="9aee9-124">Arm Resource Identifier of a Api Schema.</span></span> <span data-ttu-id="9aee9-125">Om det här alternativet anges kommer API-schema att hittas med identifieraren.</span><span class="sxs-lookup"><span data-stu-id="9aee9-125">If specified will try to find api schema by the identifier.</span></span> <span data-ttu-id="9aee9-126">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="9aee9-126">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9aee9-127">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="9aee9-127">-SchemaId</span></span>
<span data-ttu-id="9aee9-128">ID för schemat.</span><span class="sxs-lookup"><span data-stu-id="9aee9-128">The identifier of the Schema.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9aee9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9aee9-129">CommonParameters</span></span>
<span data-ttu-id="9aee9-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9aee9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9aee9-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9aee9-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9aee9-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9aee9-132">INPUTS</span></span>

### <span data-ttu-id="9aee9-133">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9aee9-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9aee9-134">System. String</span><span class="sxs-lookup"><span data-stu-id="9aee9-134">System.String</span></span>

## <span data-ttu-id="9aee9-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9aee9-135">OUTPUTS</span></span>

### <span data-ttu-id="9aee9-136">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="9aee9-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

## <span data-ttu-id="9aee9-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9aee9-137">NOTES</span></span>

## <span data-ttu-id="9aee9-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9aee9-138">RELATED LINKS</span></span>

[<span data-ttu-id="9aee9-139">New-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="9aee9-139">New-AzApiManagementApiSchema</span></span>](./New-AzApiManagementApiSchema.md)

[<span data-ttu-id="9aee9-140">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="9aee9-140">Remove-AzApiManagementApiSchema</span></span>](./Remove-AzApiManagementApiSchema.md)

[<span data-ttu-id="9aee9-141">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="9aee9-141">Set-AzApiManagementApiSchema</span></span>](./Set-AzApiManagementApiSchema.md)