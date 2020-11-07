---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiSchema.md
ms.openlocfilehash: 02091c1a207bc10fbdb539fb9a301d002b631827
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745675"
---
# <span data-ttu-id="30a5e-101">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="30a5e-101">Set-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="30a5e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="30a5e-102">SYNOPSIS</span></span>
<span data-ttu-id="30a5e-103">Ändrar ett API-schema</span><span class="sxs-lookup"><span data-stu-id="30a5e-103">Modifies an API Schema</span></span>

## <span data-ttu-id="30a5e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="30a5e-104">SYNTAX</span></span>

### <span data-ttu-id="30a5e-105">ExpandedParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="30a5e-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> -SchemaId <String>
 [-SchemaDocumentContentType <String>] [-SchemaDocument <String>] [-SchemaDocumentFilePath <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30a5e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="30a5e-106">ByInputObject</span></span>
```
Set-AzApiManagementApiSchema -InputObject <PsApiManagementApiSchema> [-SchemaDocumentContentType <String>]
 [-SchemaDocument <String>] [-SchemaDocumentFilePath <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30a5e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="30a5e-107">ByResourceId</span></span>
```
Set-AzApiManagementApiSchema -ResourceId <String> [-SchemaDocumentContentType <String>]
 [-SchemaDocument <String>] [-SchemaDocumentFilePath <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30a5e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="30a5e-108">DESCRIPTION</span></span>
<span data-ttu-id="30a5e-109">Cmdleten **set-AzApiManagementApiSchema** ändrar ett API-schema för Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="30a5e-109">The **Set-AzApiManagementApiSchema** cmdlet modifies an Azure API Management API Schema.</span></span>

## <span data-ttu-id="30a5e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="30a5e-110">EXAMPLES</span></span>

### <span data-ttu-id="30a5e-111">Exempel 1: ändrar ett API-schema</span><span class="sxs-lookup"><span data-stu-id="30a5e-111">Example 1 : Modifies an API Schema</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiSchema -Context $ApiMgmtContext -ApiId "echo-api" -SchemaId "2"
```

<span data-ttu-id="30a5e-112">Exemplet uppdaterar API-schemat</span><span class="sxs-lookup"><span data-stu-id="30a5e-112">The example updates the Api Schema</span></span>

## <span data-ttu-id="30a5e-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="30a5e-113">PARAMETERS</span></span>

### <span data-ttu-id="30a5e-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="30a5e-114">-ApiId</span></span>
<span data-ttu-id="30a5e-115">Identifierare för befintligt API.</span><span class="sxs-lookup"><span data-stu-id="30a5e-115">Identifier of existing API.</span></span>
<span data-ttu-id="30a5e-116">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="30a5e-116">This parameter is required.</span></span>

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

### <span data-ttu-id="30a5e-117">-Kontext</span><span class="sxs-lookup"><span data-stu-id="30a5e-117">-Context</span></span>
<span data-ttu-id="30a5e-118">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="30a5e-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="30a5e-119">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="30a5e-119">This parameter is required.</span></span>

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

### <span data-ttu-id="30a5e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30a5e-120">-DefaultProfile</span></span>
<span data-ttu-id="30a5e-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="30a5e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30a5e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="30a5e-122">-InputObject</span></span>
<span data-ttu-id="30a5e-123">Instans av PsApiManagementApiSchema.</span><span class="sxs-lookup"><span data-stu-id="30a5e-123">Instance of PsApiManagementApiSchema.</span></span>
<span data-ttu-id="30a5e-124">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="30a5e-124">This parameter is required.</span></span>

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

### <span data-ttu-id="30a5e-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="30a5e-125">-PassThru</span></span>
<span data-ttu-id="30a5e-126">Om det anges kommer instansen av Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi typ som representerar set API.</span><span class="sxs-lookup"><span data-stu-id="30a5e-126">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi type representing the set API.</span></span>

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

### <span data-ttu-id="30a5e-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="30a5e-127">-ResourceId</span></span>
<span data-ttu-id="30a5e-128">Arm-ResourceId för diagnostiskt eller API-schema.</span><span class="sxs-lookup"><span data-stu-id="30a5e-128">Arm ResourceId of Diagnostic or Api Schema.</span></span> <span data-ttu-id="30a5e-129">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="30a5e-129">This parameter is required.</span></span>

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

### <span data-ttu-id="30a5e-130">-SchemaDocument</span><span class="sxs-lookup"><span data-stu-id="30a5e-130">-SchemaDocument</span></span>
<span data-ttu-id="30a5e-131">API-schema dokumentet som en sträng.</span><span class="sxs-lookup"><span data-stu-id="30a5e-131">Api schema document as a string.</span></span> <span data-ttu-id="30a5e-132">Den här parametern är obligatorisk-SchemaDocumentFile har inte angetts.</span><span class="sxs-lookup"><span data-stu-id="30a5e-132">This parameter is required is -SchemaDocumentFile is not specified.</span></span>

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

### <span data-ttu-id="30a5e-133">-SchemaDocumentContentType</span><span class="sxs-lookup"><span data-stu-id="30a5e-133">-SchemaDocumentContentType</span></span>
<span data-ttu-id="30a5e-134">ContentType för API-schema.</span><span class="sxs-lookup"><span data-stu-id="30a5e-134">ContentType of the api Schema.</span></span> <span data-ttu-id="30a5e-135">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="30a5e-135">This parameter is optional.</span></span>

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

### <span data-ttu-id="30a5e-136">-SchemaDocumentFilePath</span><span class="sxs-lookup"><span data-stu-id="30a5e-136">-SchemaDocumentFilePath</span></span>
<span data-ttu-id="30a5e-137">Sökväg till dokument filen för API-schema.</span><span class="sxs-lookup"><span data-stu-id="30a5e-137">Api schema document file path.</span></span> <span data-ttu-id="30a5e-138">Den här parametern är obligatorisk-SchemaDocument har inte angetts.</span><span class="sxs-lookup"><span data-stu-id="30a5e-138">This parameter is required is -SchemaDocument is not specified.</span></span>

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

### <span data-ttu-id="30a5e-139">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="30a5e-139">-SchemaId</span></span>
<span data-ttu-id="30a5e-140">Identifierare för befintligt schema.</span><span class="sxs-lookup"><span data-stu-id="30a5e-140">Identifier of existing Schema.</span></span>
<span data-ttu-id="30a5e-141">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="30a5e-141">This parameter is required.</span></span>

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

### <span data-ttu-id="30a5e-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="30a5e-142">-Confirm</span></span>
<span data-ttu-id="30a5e-143">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="30a5e-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30a5e-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30a5e-144">-WhatIf</span></span>
<span data-ttu-id="30a5e-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="30a5e-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="30a5e-146">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="30a5e-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30a5e-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30a5e-147">CommonParameters</span></span>
<span data-ttu-id="30a5e-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30a5e-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30a5e-149">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="30a5e-149">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30a5e-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="30a5e-150">INPUTS</span></span>

### <span data-ttu-id="30a5e-151">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="30a5e-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="30a5e-152">System. String</span><span class="sxs-lookup"><span data-stu-id="30a5e-152">System.String</span></span>

### <span data-ttu-id="30a5e-153">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="30a5e-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

### <span data-ttu-id="30a5e-154">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="30a5e-154">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="30a5e-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="30a5e-155">OUTPUTS</span></span>

### <span data-ttu-id="30a5e-156">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="30a5e-156">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="30a5e-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="30a5e-157">NOTES</span></span>

## <span data-ttu-id="30a5e-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="30a5e-158">RELATED LINKS</span></span>

[<span data-ttu-id="30a5e-159">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="30a5e-159">Get-AzApiManagementApiSchema</span></span>](./Get-AzApiManagementApiSchema.md)

[<span data-ttu-id="30a5e-160">New-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="30a5e-160">New-AzApiManagementApiSchema</span></span>](./New-AzApiManagementApiSchema.md)

[<span data-ttu-id="30a5e-161">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="30a5e-161">Remove-AzApiManagementApiSchema</span></span>](./Remove-AzApiManagementApiSchema.md)

