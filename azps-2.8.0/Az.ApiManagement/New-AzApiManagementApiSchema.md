---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiSchema.md
ms.openlocfilehash: de1cee21dede597833ea2940775ac6ccee22e0ea
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745794"
---
# <span data-ttu-id="db368-101">New-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="db368-101">New-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="db368-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="db368-102">SYNOPSIS</span></span>
<span data-ttu-id="db368-103">Skapar det nya API-schemat i ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="db368-103">Creates the new API Schema in the ApiManagement service</span></span>

## <span data-ttu-id="db368-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="db368-104">SYNTAX</span></span>

### <span data-ttu-id="db368-105">SchemaDocumentInline (standard)</span><span class="sxs-lookup"><span data-stu-id="db368-105">SchemaDocumentInline (Default)</span></span>
```
New-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 -SchemaDocumentContentType <String> -SchemaDocument <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db368-106">SchemaDocumentFromFile</span><span class="sxs-lookup"><span data-stu-id="db368-106">SchemaDocumentFromFile</span></span>
```
New-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 -SchemaDocumentContentType <String> -SchemaDocumentFilePath <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db368-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="db368-107">DESCRIPTION</span></span>
<span data-ttu-id="db368-108">Skapar det nya API-schemat för API: t.</span><span class="sxs-lookup"><span data-stu-id="db368-108">Creates the new API Schema of the API.</span></span>

## <span data-ttu-id="db368-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="db368-109">EXAMPLES</span></span>

### <span data-ttu-id="db368-110">Exempel 1: skapa ett nytt schema för Swagger petstore omfattande API</span><span class="sxs-lookup"><span data-stu-id="db368-110">Example 1 : Create new Schema for Swagger Petstore Extensive API</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/resourceGroupName/providers/Microsoft.ApiManagement/service/sdktestapim4163
PS D:\github\azure-powershell> New-AzApiManagementApiSchema -Context $context -ApiId swagger-petstore-extensive -SchemaDocumentContentType swaggerdefinition -SchemaDocumentFilePath C:\Users\sasolank\Downloads\petstoreschema.json
Schema Id                            Api Id                     Schema ContentType
---------                            ------                     ------------------
3e8892eb-98e4-408d-b77a-f424185c1044 swagger-petstore-extensive swaggerdefinition
```

<span data-ttu-id="db368-111">Cmdlet **New-AzApiManagementApiSchema** skapar eller uppdaterar schemat för `swagger-petstore-extensive` aPI: t.</span><span class="sxs-lookup"><span data-stu-id="db368-111">The cmdlet **New-AzApiManagementApiSchema** creates or updates the schema of the `swagger-petstore-extensive` aPI.</span></span>

## <span data-ttu-id="db368-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="db368-112">PARAMETERS</span></span>

### <span data-ttu-id="db368-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="db368-113">-ApiId</span></span>
<span data-ttu-id="db368-114">ID för API.</span><span class="sxs-lookup"><span data-stu-id="db368-114">Identifier of api.</span></span> <span data-ttu-id="db368-115">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="db368-115">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db368-116">-Kontext</span><span class="sxs-lookup"><span data-stu-id="db368-116">-Context</span></span>
<span data-ttu-id="db368-117">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="db368-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="db368-118">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="db368-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db368-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db368-119">-DefaultProfile</span></span>
<span data-ttu-id="db368-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="db368-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db368-121">-SchemaDocument</span><span class="sxs-lookup"><span data-stu-id="db368-121">-SchemaDocument</span></span>
<span data-ttu-id="db368-122">API-schema dokumentet som en sträng.</span><span class="sxs-lookup"><span data-stu-id="db368-122">Api schema document as a string.</span></span> <span data-ttu-id="db368-123">Den här parametern är obligatorisk-SchemaDocumentFile har inte angetts.</span><span class="sxs-lookup"><span data-stu-id="db368-123">This parameter is required is -SchemaDocumentFile is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: SchemaDocumentInline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db368-124">-SchemaDocumentContentType</span><span class="sxs-lookup"><span data-stu-id="db368-124">-SchemaDocumentContentType</span></span>
<span data-ttu-id="db368-125">ContentType för API-schema.</span><span class="sxs-lookup"><span data-stu-id="db368-125">ContentType of the api Schema.</span></span> <span data-ttu-id="db368-126">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="db368-126">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db368-127">-SchemaDocumentFilePath</span><span class="sxs-lookup"><span data-stu-id="db368-127">-SchemaDocumentFilePath</span></span>
<span data-ttu-id="db368-128">Sökväg till dokument filen för API-schema.</span><span class="sxs-lookup"><span data-stu-id="db368-128">Api schema document file path.</span></span> <span data-ttu-id="db368-129">Den här parametern är obligatorisk-SchemaDocument har inte angetts.</span><span class="sxs-lookup"><span data-stu-id="db368-129">This parameter is required is -SchemaDocument is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: SchemaDocumentFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db368-130">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="db368-130">-SchemaId</span></span>
<span data-ttu-id="db368-131">Identifierare för nytt schema.</span><span class="sxs-lookup"><span data-stu-id="db368-131">Identifier of new schema.</span></span>
<span data-ttu-id="db368-132">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="db368-132">This parameter is optional.</span></span>
<span data-ttu-id="db368-133">Om det inte anges kommer att genereras.</span><span class="sxs-lookup"><span data-stu-id="db368-133">If not specified will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db368-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="db368-134">-Confirm</span></span>
<span data-ttu-id="db368-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="db368-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db368-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db368-136">-WhatIf</span></span>
<span data-ttu-id="db368-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="db368-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db368-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="db368-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db368-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db368-139">CommonParameters</span></span>
<span data-ttu-id="db368-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db368-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db368-141">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="db368-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db368-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="db368-142">INPUTS</span></span>

### <span data-ttu-id="db368-143">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="db368-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="db368-144">System. String</span><span class="sxs-lookup"><span data-stu-id="db368-144">System.String</span></span>

## <span data-ttu-id="db368-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="db368-145">OUTPUTS</span></span>

### <span data-ttu-id="db368-146">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="db368-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

## <span data-ttu-id="db368-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="db368-147">NOTES</span></span>

## <span data-ttu-id="db368-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="db368-148">RELATED LINKS</span></span>

[<span data-ttu-id="db368-149">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="db368-149">Get-AzApiManagementApiSchema</span></span>](./Get-AzApiManagementApiSchema.md)

[<span data-ttu-id="db368-150">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="db368-150">Remove-AzApiManagementApiSchema</span></span>](./Remove-AzApiManagementApiSchema.md)

[<span data-ttu-id="db368-151">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="db368-151">Set-AzApiManagementApiSchema</span></span>](./Set-AzApiManagementApiSchema.md)
