---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiSchema.md
ms.openlocfilehash: ec27180cbe256f8cd102fd4f62409d449d885bd2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325392"
---
# <span data-ttu-id="09a6e-101">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="09a6e-101">Set-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="09a6e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="09a6e-102">SYNOPSIS</span></span>
<span data-ttu-id="09a6e-103">Ändrar ett API-schema</span><span class="sxs-lookup"><span data-stu-id="09a6e-103">Modifies an API Schema</span></span>

## <span data-ttu-id="09a6e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="09a6e-104">SYNTAX</span></span>

### <span data-ttu-id="09a6e-105">ExpandedParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="09a6e-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> -SchemaId <String>
 [-SchemaDocumentContentType <String>] [-SchemaDocument <String>] [-SchemaDocumentFilePath <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09a6e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="09a6e-106">ByInputObject</span></span>
```
Set-AzApiManagementApiSchema -InputObject <PsApiManagementApiSchema> [-SchemaDocumentContentType <String>]
 [-SchemaDocument <String>] [-SchemaDocumentFilePath <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09a6e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="09a6e-107">ByResourceId</span></span>
```
Set-AzApiManagementApiSchema -ResourceId <String> [-SchemaDocumentContentType <String>]
 [-SchemaDocument <String>] [-SchemaDocumentFilePath <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09a6e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="09a6e-108">DESCRIPTION</span></span>
<span data-ttu-id="09a6e-109">Cmdleten **set-AzApiManagementApiSchema** ändrar ett API-schema för Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="09a6e-109">The **Set-AzApiManagementApiSchema** cmdlet modifies an Azure API Management API Schema.</span></span>

## <span data-ttu-id="09a6e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="09a6e-110">EXAMPLES</span></span>

### <span data-ttu-id="09a6e-111">Exempel 1: ändrar ett API-schema</span><span class="sxs-lookup"><span data-stu-id="09a6e-111">Example 1: Modifies an API Schema</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiSchema -Context $ApiMgmtContext -ApiId "echo-api" -SchemaId "2"
```

<span data-ttu-id="09a6e-112">Exemplet uppdaterar API-schemat</span><span class="sxs-lookup"><span data-stu-id="09a6e-112">The example updates the Api Schema</span></span>

### <span data-ttu-id="09a6e-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="09a6e-113">Example 2</span></span>

<span data-ttu-id="09a6e-114">Ändrar ett API-schema.</span><span class="sxs-lookup"><span data-stu-id="09a6e-114">Modifies an API Schema.</span></span> <span data-ttu-id="09a6e-115">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="09a6e-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzApiManagementApiSchema -ApiId 'echo-api' -Context <PsApiManagementContext> -SchemaDocumentContentType swaggerdefinition -SchemaDocumentFilePath C:\Users\sasolank\Downloads\petstoreschema.json -SchemaId '2'
```

## <span data-ttu-id="09a6e-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="09a6e-116">PARAMETERS</span></span>

### <span data-ttu-id="09a6e-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="09a6e-117">-ApiId</span></span>
<span data-ttu-id="09a6e-118">Identifierare för befintligt API.</span><span class="sxs-lookup"><span data-stu-id="09a6e-118">Identifier of existing API.</span></span>
<span data-ttu-id="09a6e-119">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="09a6e-119">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09a6e-120">-Kontext</span><span class="sxs-lookup"><span data-stu-id="09a6e-120">-Context</span></span>
<span data-ttu-id="09a6e-121">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="09a6e-121">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="09a6e-122">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="09a6e-122">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09a6e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09a6e-123">-DefaultProfile</span></span>
<span data-ttu-id="09a6e-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="09a6e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09a6e-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09a6e-125">-InputObject</span></span>
<span data-ttu-id="09a6e-126">Instans av PsApiManagementApiSchema.</span><span class="sxs-lookup"><span data-stu-id="09a6e-126">Instance of PsApiManagementApiSchema.</span></span>
<span data-ttu-id="09a6e-127">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="09a6e-127">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09a6e-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="09a6e-128">-PassThru</span></span>
<span data-ttu-id="09a6e-129">Om det anges kommer instansen av Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi typ som representerar set API.</span><span class="sxs-lookup"><span data-stu-id="09a6e-129">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi type representing the set API.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09a6e-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="09a6e-130">-ResourceId</span></span>
<span data-ttu-id="09a6e-131">Arm-ResourceId för diagnostiskt eller API-schema.</span><span class="sxs-lookup"><span data-stu-id="09a6e-131">Arm ResourceId of Diagnostic or Api Schema.</span></span> <span data-ttu-id="09a6e-132">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="09a6e-132">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09a6e-133">-SchemaDocument</span><span class="sxs-lookup"><span data-stu-id="09a6e-133">-SchemaDocument</span></span>
<span data-ttu-id="09a6e-134">API-schema dokumentet som en sträng.</span><span class="sxs-lookup"><span data-stu-id="09a6e-134">Api schema document as a string.</span></span> <span data-ttu-id="09a6e-135">Den här parametern är obligatorisk-SchemaDocumentFile har inte angetts.</span><span class="sxs-lookup"><span data-stu-id="09a6e-135">This parameter is required is -SchemaDocumentFile is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09a6e-136">-SchemaDocumentContentType</span><span class="sxs-lookup"><span data-stu-id="09a6e-136">-SchemaDocumentContentType</span></span>
<span data-ttu-id="09a6e-137">ContentType för API-schema.</span><span class="sxs-lookup"><span data-stu-id="09a6e-137">ContentType of the api Schema.</span></span> <span data-ttu-id="09a6e-138">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="09a6e-138">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09a6e-139">-SchemaDocumentFilePath</span><span class="sxs-lookup"><span data-stu-id="09a6e-139">-SchemaDocumentFilePath</span></span>
<span data-ttu-id="09a6e-140">Sökväg till dokument filen för API-schema.</span><span class="sxs-lookup"><span data-stu-id="09a6e-140">Api schema document file path.</span></span> <span data-ttu-id="09a6e-141">Den här parametern är obligatorisk-SchemaDocument har inte angetts.</span><span class="sxs-lookup"><span data-stu-id="09a6e-141">This parameter is required is -SchemaDocument is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09a6e-142">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="09a6e-142">-SchemaId</span></span>
<span data-ttu-id="09a6e-143">Identifierare för befintligt schema.</span><span class="sxs-lookup"><span data-stu-id="09a6e-143">Identifier of existing Schema.</span></span>
<span data-ttu-id="09a6e-144">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="09a6e-144">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09a6e-145">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="09a6e-145">-Confirm</span></span>
<span data-ttu-id="09a6e-146">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="09a6e-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09a6e-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09a6e-147">-WhatIf</span></span>
<span data-ttu-id="09a6e-148">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="09a6e-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="09a6e-149">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="09a6e-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09a6e-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09a6e-150">CommonParameters</span></span>
<span data-ttu-id="09a6e-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09a6e-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09a6e-152">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="09a6e-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09a6e-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="09a6e-153">INPUTS</span></span>

### <span data-ttu-id="09a6e-154">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="09a6e-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="09a6e-155">System. String</span><span class="sxs-lookup"><span data-stu-id="09a6e-155">System.String</span></span>

### <span data-ttu-id="09a6e-156">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="09a6e-156">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

### <span data-ttu-id="09a6e-157">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="09a6e-157">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="09a6e-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="09a6e-158">OUTPUTS</span></span>

### <span data-ttu-id="09a6e-159">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="09a6e-159">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="09a6e-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="09a6e-160">NOTES</span></span>

## <span data-ttu-id="09a6e-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="09a6e-161">RELATED LINKS</span></span>

[<span data-ttu-id="09a6e-162">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="09a6e-162">Get-AzApiManagementApiSchema</span></span>](./Get-AzApiManagementApiSchema.md)

[<span data-ttu-id="09a6e-163">New-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="09a6e-163">New-AzApiManagementApiSchema</span></span>](./New-AzApiManagementApiSchema.md)

[<span data-ttu-id="09a6e-164">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="09a6e-164">Remove-AzApiManagementApiSchema</span></span>](./Remove-AzApiManagementApiSchema.md)
