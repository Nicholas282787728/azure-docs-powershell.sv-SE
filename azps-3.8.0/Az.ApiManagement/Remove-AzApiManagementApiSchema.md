---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiSchema.md
ms.openlocfilehash: fb144bfa228b07501c374f054970d1e3e0337ec1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092795"
---
# <span data-ttu-id="bfca9-101">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="bfca9-101">Remove-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="bfca9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bfca9-102">SYNOPSIS</span></span>
<span data-ttu-id="bfca9-103">Tar bort API-schema från API: t.</span><span class="sxs-lookup"><span data-stu-id="bfca9-103">Removes the API Schema from the API.</span></span>

## <span data-ttu-id="bfca9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bfca9-104">SYNTAX</span></span>

### <span data-ttu-id="bfca9-105">ByApiSchemaId (standard)</span><span class="sxs-lookup"><span data-stu-id="bfca9-105">ByApiSchemaId (Default)</span></span>
```
Remove-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> -SchemaId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfca9-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="bfca9-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiSchema -InputObject <PsApiManagementApiSchema> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfca9-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bfca9-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementApiSchema -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfca9-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bfca9-108">DESCRIPTION</span></span>
<span data-ttu-id="bfca9-109">Cmdlet **Remove-AzApiManagementSchema** från API.</span><span class="sxs-lookup"><span data-stu-id="bfca9-109">The cmdlet **Remove-AzApiManagementSchema** from the Api.</span></span>

## <span data-ttu-id="bfca9-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bfca9-110">EXAMPLES</span></span>

### <span data-ttu-id="bfca9-111">Exempel 1: tar bort API-schemat från API</span><span class="sxs-lookup"><span data-stu-id="bfca9-111">Example 1 : Removes the Api Schema from the API</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzAzureRmApiManagementApiSchema -Context $apimContext -ApiId "echo-api" -SchemaId "2"
```

<span data-ttu-id="bfca9-112">Skriptet tar bort schemat `2` från API: t `echo-api` om det inte refereras till.</span><span class="sxs-lookup"><span data-stu-id="bfca9-112">The script removes the Schema `2` from the Api `echo-api` if it is not referenced.</span></span>

## <span data-ttu-id="bfca9-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bfca9-113">PARAMETERS</span></span>

### <span data-ttu-id="bfca9-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="bfca9-114">-ApiId</span></span>
<span data-ttu-id="bfca9-115">ID för API: t.</span><span class="sxs-lookup"><span data-stu-id="bfca9-115">Identifier of the API.</span></span>
<span data-ttu-id="bfca9-116">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="bfca9-116">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiSchemaId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfca9-117">-Kontext</span><span class="sxs-lookup"><span data-stu-id="bfca9-117">-Context</span></span>
<span data-ttu-id="bfca9-118">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="bfca9-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="bfca9-119">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="bfca9-119">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ByApiSchemaId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bfca9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfca9-120">-DefaultProfile</span></span>
<span data-ttu-id="bfca9-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bfca9-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bfca9-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bfca9-122">-InputObject</span></span>
<span data-ttu-id="bfca9-123">Instans av PsApiManagementApiSchema.</span><span class="sxs-lookup"><span data-stu-id="bfca9-123">Instance of PsApiManagementApiSchema.</span></span>
<span data-ttu-id="bfca9-124">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="bfca9-124">This parameter is required.</span></span>

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

### <span data-ttu-id="bfca9-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bfca9-125">-PassThru</span></span>
<span data-ttu-id="bfca9-126">Om det här värdet anges skrivs sant om-operationen lyckas.</span><span class="sxs-lookup"><span data-stu-id="bfca9-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="bfca9-127">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="bfca9-127">This parameter is optional.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfca9-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bfca9-128">-ResourceId</span></span>
<span data-ttu-id="bfca9-129">ResourceId för ApiSchema.</span><span class="sxs-lookup"><span data-stu-id="bfca9-129">Arm ResourceId of ApiSchema.</span></span> <span data-ttu-id="bfca9-130">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="bfca9-130">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfca9-131">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="bfca9-131">-SchemaId</span></span>
<span data-ttu-id="bfca9-132">Identifierare för API-schema.</span><span class="sxs-lookup"><span data-stu-id="bfca9-132">Identifier of the API Schema.</span></span>
<span data-ttu-id="bfca9-133">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="bfca9-133">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiSchemaId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfca9-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bfca9-134">-Confirm</span></span>
<span data-ttu-id="bfca9-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bfca9-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfca9-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfca9-136">-WhatIf</span></span>
<span data-ttu-id="bfca9-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bfca9-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfca9-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bfca9-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfca9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfca9-139">CommonParameters</span></span>
<span data-ttu-id="bfca9-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfca9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfca9-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bfca9-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfca9-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bfca9-142">INPUTS</span></span>

### <span data-ttu-id="bfca9-143">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="bfca9-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="bfca9-144">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="bfca9-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

### <span data-ttu-id="bfca9-145">System. String</span><span class="sxs-lookup"><span data-stu-id="bfca9-145">System.String</span></span>

## <span data-ttu-id="bfca9-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bfca9-146">OUTPUTS</span></span>

### <span data-ttu-id="bfca9-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bfca9-147">System.Boolean</span></span>

## <span data-ttu-id="bfca9-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bfca9-148">NOTES</span></span>

## <span data-ttu-id="bfca9-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bfca9-149">RELATED LINKS</span></span>

[<span data-ttu-id="bfca9-150">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="bfca9-150">Get-AzApiManagementApiSchema</span></span>](./Get-AzApiManagementApiSchema.md)

[<span data-ttu-id="bfca9-151">New-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="bfca9-151">New-AzApiManagementApiSchema</span></span>](./New-AzApiManagementApiSchema.md)

[<span data-ttu-id="bfca9-152">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="bfca9-152">Set-AzApiManagementApiSchema</span></span>](./Set-AzApiManagementApiSchema.md)
