---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/set-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Set-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Set-AzHealthcareApisService.md
ms.openlocfilehash: 36632398d95acdd16d2a7b41c09bed7172391639
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744036"
---
# <span data-ttu-id="7a1ec-101">Set-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="7a1ec-101">Set-AzHealthcareApisService</span></span>

## <span data-ttu-id="7a1ec-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7a1ec-102">SYNOPSIS</span></span>
<span data-ttu-id="7a1ec-103">Uppdaterar en befintlig healthcareApis FHIR-tjänst.</span><span class="sxs-lookup"><span data-stu-id="7a1ec-103">Updates an existing healthcareApis fhir service.</span></span>

## <span data-ttu-id="7a1ec-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7a1ec-104">SYNTAX</span></span>

### <span data-ttu-id="7a1ec-105">ServiceNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="7a1ec-105">ServiceNameParameterSet (Default)</span></span>
```
Set-AzHealthcareApisService -Name <String> -ResourceGroupName <String> [-CosmosOfferThroughput <Int32>]
 [-Authority <String>] [-Audience <String>] [-EnableSmartProxy] [-DisableSmartProxy] [-CorsOrigin <String[]>]
 [-CorsHeader <String[]>] [-CorsMethod <String[]>] [-CorsMaxAge <Int32>] [-AllowCorsCredential]
 [-DisableCorsCredential] [-AccessPolicyObjectId <String[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a1ec-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a1ec-106">ResourceIdParameterSet</span></span>
```
Set-AzHealthcareApisService [-CosmosOfferThroughput <Int32>] [-Authority <String>] [-Audience <String>]
 [-EnableSmartProxy] [-DisableSmartProxy] [-CorsOrigin <String[]>] [-CorsHeader <String[]>]
 [-CorsMethod <String[]>] [-CorsMaxAge <Int32>] [-AllowCorsCredential] [-DisableCorsCredential]
 [-AccessPolicyObjectId <String[]>] [-Tag <Hashtable>] -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a1ec-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a1ec-107">InputObjectParameterSet</span></span>
```
Set-AzHealthcareApisService -InputObject <PSHealthcareApisService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a1ec-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7a1ec-108">DESCRIPTION</span></span>
<span data-ttu-id="7a1ec-109">Uppdaterar en befintlig healthcareApis FHIR-tjänst.</span><span class="sxs-lookup"><span data-stu-id="7a1ec-109">Updates an existing healthcareApis fhir service.</span></span>

## <span data-ttu-id="7a1ec-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7a1ec-110">EXAMPLES</span></span>

### <span data-ttu-id="7a1ec-111">Exempel 1: uppdaterar den befintliga healthcareapis-tjänsten i resurs gruppen MyResourceGroup med cosmosdb OfferThroughput = 500.</span><span class="sxs-lookup"><span data-stu-id="7a1ec-111">Example 1 : Updates the existing healthcareapis service named MyService in the resource group MyResourceGroup  with the cosmosdb OfferThroughput = 500.</span></span>

```powershell
PS C:\> Set-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup -CosmosOfferThroughput 500

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbOfferThroughput : 500
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False
```

### <span data-ttu-id="7a1ec-112">Exempel 2: uppdaterar den befintliga healthcareapis-tjänsten i resurs gruppen MyResourceGroup med cosmosdb OfferThroughput = 500.</span><span class="sxs-lookup"><span data-stu-id="7a1ec-112">Example 2: Updates the existing healthcareapis service named MyService in the resource group MyResourceGroup  with the cosmosdb OfferThroughput = 500.</span></span>

```powershell
PS C:\> $ResourceId = "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.HealthcareApis/services/MyService"
PS C:\> Set-AzHealthcareApisService -ResourceId $ResourceId  -CosmosOfferThroughput 500

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbOfferThroughput : 500
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False
```

## <span data-ttu-id="7a1ec-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7a1ec-113">PARAMETERS</span></span>

### <span data-ttu-id="7a1ec-114">-AccessPolicyObjectId</span><span class="sxs-lookup"><span data-stu-id="7a1ec-114">-AccessPolicyObjectId</span></span>
<span data-ttu-id="7a1ec-115">Lista över objekt-ID: n för Access policy.</span><span class="sxs-lookup"><span data-stu-id="7a1ec-115">List of Access Policy Object IDs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a1ec-116">-AllowCorsCredential</span><span class="sxs-lookup"><span data-stu-id="7a1ec-116">-AllowCorsCredential</span></span>
<span data-ttu-id="7a1ec-117">HealthcareApis FhirService AllowCorsCredential.</span><span class="sxs-lookup"><span data-stu-id="7a1ec-117">HealthcareApis FhirService AllowCorsCredential.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a1ec-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7a1ec-118">-AsJob</span></span>
<span data-ttu-id="7a1ec-119">Kör cmdlet som ett jobb i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="7a1ec-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="7a1ec-120">-Åhörare</span><span class="sxs-lookup"><span data-stu-id="7a1ec-120">-Audience</span></span>
<span data-ttu-id="7a1ec-121">HealthcareApis FhirService mål grupp.</span><span class="sxs-lookup"><span data-stu-id="7a1ec-121">HealthcareApis FhirService Audience.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a1ec-122">-Myndighet</span><span class="sxs-lookup"><span data-stu-id="7a1ec-122">-Authority</span></span>
<span data-ttu-id="7a1ec-123">HealthcareApis FhirService-myndighet.</span><span class="sxs-lookup"><span data-stu-id="7a1ec-123">HealthcareApis FhirService Authority.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a1ec-124">-CorsHeader</span><span class="sxs-lookup"><span data-stu-id="7a1ec-124">-CorsHeader</span></span>
<span data-ttu-id="7a1ec-125">HealthcareApis FHIR tjänst lista över CORS-rubriker.</span><span class="sxs-lookup"><span data-stu-id="7a1ec-125">HealthcareApis Fhir Service List of Cors Header.</span></span> <span data-ttu-id="7a1ec-126">Ange HTTP-huvuden som kan användas under begäran.</span><span class="sxs-lookup"><span data-stu-id="7a1ec-126">Specify HTTP headers which can be used during the request.</span></span> <span data-ttu-id="7a1ec-127">Använd \* för alla sidhuvuden.</span><span class="sxs-lookup"><span data-stu-id="7a1ec-127">Use \* for any header.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a1ec-128">-CorsMaxAge</span><span class="sxs-lookup"><span data-stu-id="7a1ec-128">-CorsMaxAge</span></span>
<span data-ttu-id="7a1ec-129">HealthcareApis FHIR tjänst CORS Max åldern.</span><span class="sxs-lookup"><span data-stu-id="7a1ec-129">HealthcareApis Fhir Service Cors Max Age.</span></span> <span data-ttu-id="7a1ec-130">Ange hur lång tid ett resultat från en begäran kan cachelagras på några sekunder.</span><span class="sxs-lookup"><span data-stu-id="7a1ec-130">Specify how long a result from a request can be cached in seconds.</span></span> <span data-ttu-id="7a1ec-131">Exempel: 600 betyder 10 minuter.</span><span class="sxs-lookup"><span data-stu-id="7a1ec-131">Example: 600 means 10 minutes.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a1ec-132">-CorsMethod</span><span class="sxs-lookup"><span data-stu-id="7a1ec-132">-CorsMethod</span></span>
<span data-ttu-id="7a1ec-133">HealthcareApis FhirService lista med CORS-metoder.</span><span class="sxs-lookup"><span data-stu-id="7a1ec-133">HealthcareApis FhirService List of Cors Methods.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:
Accepted values: DELETE, GET, OPTIONS, PATCH, POST, PUT

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a1ec-134">-CorsOrigin</span><span class="sxs-lookup"><span data-stu-id="7a1ec-134">-CorsOrigin</span></span>
<span data-ttu-id="7a1ec-135">HealthcareApis FhirService lista med CORS-ursprung.</span><span class="sxs-lookup"><span data-stu-id="7a1ec-135">HealthcareApis FhirService List of Cors Origins.</span></span> <span data-ttu-id="7a1ec-136">HealthcareApis FHIR tjänst lista över CORS Origine.</span><span class="sxs-lookup"><span data-stu-id="7a1ec-136">HealthcareApis Fhir Service List of Cors Origin.</span></span> <span data-ttu-id="7a1ec-137">Ange URL: er för ursprungs webbplatser som har till gång till detta API eller Använd \* för att tillåta åtkomst från vilken webbplats som helst.</span><span class="sxs-lookup"><span data-stu-id="7a1ec-137">Specify URLs of origin sites that can access this API, or use \* to allow access from any site.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a1ec-138">-CosmosOfferThroughput</span><span class="sxs-lookup"><span data-stu-id="7a1ec-138">-CosmosOfferThroughput</span></span>
<span data-ttu-id="7a1ec-139">HealthcareApis FhirService CosmosOfferThroughput.</span><span class="sxs-lookup"><span data-stu-id="7a1ec-139">HealthcareApis FhirService CosmosOfferThroughput.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a1ec-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a1ec-140">-DefaultProfile</span></span>
<span data-ttu-id="7a1ec-141">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7a1ec-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a1ec-142">-DisableCorsCredential</span><span class="sxs-lookup"><span data-stu-id="7a1ec-142">-DisableCorsCredential</span></span>
<span data-ttu-id="7a1ec-143">HealthcareApis FhirService CorsCredentials är inte tillåtet.</span><span class="sxs-lookup"><span data-stu-id="7a1ec-143">HealthcareApis FhirService CorsCredentials Not Allowed.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a1ec-144">-DisableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="7a1ec-144">-DisableSmartProxy</span></span>
<span data-ttu-id="7a1ec-145">HealthcareApis FhirService DisableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="7a1ec-145">HealthcareApis FhirService DisableSmartProxy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a1ec-146">-EnableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="7a1ec-146">-EnableSmartProxy</span></span>
<span data-ttu-id="7a1ec-147">HealthcareApis FhirService EnableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="7a1ec-147">HealthcareApis FhirService EnableSmartProxy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a1ec-148">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a1ec-148">-InputObject</span></span>
<span data-ttu-id="7a1ec-149">HealthcareApis FHIR-piped från get-AzHealthcareApisFhirService.</span><span class="sxs-lookup"><span data-stu-id="7a1ec-149">HealthcareApis fhir service piped from Get-AzHealthcareApisFhirService.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a1ec-150">-Namn</span><span class="sxs-lookup"><span data-stu-id="7a1ec-150">-Name</span></span>
<span data-ttu-id="7a1ec-151">HealthcareApis-tjänstens namn.</span><span class="sxs-lookup"><span data-stu-id="7a1ec-151">HealthcareApis Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a1ec-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a1ec-152">-ResourceGroupName</span></span>
<span data-ttu-id="7a1ec-153">HealthcareApis tjänst resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="7a1ec-153">HealthcareApis Service Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a1ec-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a1ec-154">-ResourceId</span></span>
<span data-ttu-id="7a1ec-155">HealthcareApis FHIR tjänst ResourceId.</span><span class="sxs-lookup"><span data-stu-id="7a1ec-155">HealthcareApis Fhir Service ResourceId.</span></span>

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

### <span data-ttu-id="7a1ec-156">-Tagg</span><span class="sxs-lookup"><span data-stu-id="7a1ec-156">-Tag</span></span>
<span data-ttu-id="7a1ec-157">HealthcareApis FHIR.</span><span class="sxs-lookup"><span data-stu-id="7a1ec-157">HealthcareApis Fhir Service Account Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a1ec-158">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7a1ec-158">-Confirm</span></span>
<span data-ttu-id="7a1ec-159">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7a1ec-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a1ec-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a1ec-160">-WhatIf</span></span>
<span data-ttu-id="7a1ec-161">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7a1ec-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a1ec-162">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7a1ec-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a1ec-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a1ec-163">CommonParameters</span></span>
<span data-ttu-id="7a1ec-164">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a1ec-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a1ec-165">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7a1ec-165">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a1ec-166">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7a1ec-166">INPUTS</span></span>

### <span data-ttu-id="7a1ec-167">System. String</span><span class="sxs-lookup"><span data-stu-id="7a1ec-167">System.String</span></span>

### <span data-ttu-id="7a1ec-168">Microsoft. Azure. commands. HealthcareApisService. Models. PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="7a1ec-168">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="7a1ec-169">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7a1ec-169">OUTPUTS</span></span>

### <span data-ttu-id="7a1ec-170">Microsoft. Azure. commands. HealthcareApisService. Models. PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="7a1ec-170">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="7a1ec-171">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7a1ec-171">NOTES</span></span>

## <span data-ttu-id="7a1ec-172">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7a1ec-172">RELATED LINKS</span></span>
