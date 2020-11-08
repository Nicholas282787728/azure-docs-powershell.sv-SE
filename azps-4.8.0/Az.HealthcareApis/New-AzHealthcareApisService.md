---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/new-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/New-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/New-AzHealthcareApisService.md
ms.openlocfilehash: f5f8f00a2ab73485b4da6ad6df17ecf526c360bb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262653"
---
# <span data-ttu-id="72716-101">New-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="72716-101">New-AzHealthcareApisService</span></span>

## <span data-ttu-id="72716-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="72716-102">SYNOPSIS</span></span>
<span data-ttu-id="72716-103">Skapar metadata för en tjänst instans.</span><span class="sxs-lookup"><span data-stu-id="72716-103">Creates the metadata of a service instance.</span></span>

## <span data-ttu-id="72716-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="72716-104">SYNTAX</span></span>

```
New-AzHealthcareApisService -Name <String> -ResourceGroupName <String> -Location <String> [-Kind <String>]
 [-AccessPolicyObjectId <String[]>] [-AllowCorsCredential] [-Audience <String>] [-Authority <String>]
 [-CorsHeader <String[]>] [-CorsMaxAge <Int32>] [-CorsMethod <String[]>] [-CorsOrigin <String[]>]
 [-CosmosOfferThroughput <Int32>] [-ExportStorageAccountName <String>] [-EnableSmartProxy] [-ManagedIdentity]
 [-FhirVersion <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72716-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="72716-105">DESCRIPTION</span></span>
<span data-ttu-id="72716-106">Skapar eller uppdaterar metadata för en tjänst instans.</span><span class="sxs-lookup"><span data-stu-id="72716-106">Creates or updates the metadata of a service instance.</span></span>

## <span data-ttu-id="72716-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="72716-107">EXAMPLES</span></span>

### <span data-ttu-id="72716-108">Exempel 1: skapar en ny Azure healthcareapis FHIR-tjänst som heter min tjänst i resurs gruppen MyResourceGroup på en plats westus2 med cosmosdb offer genomflöde = 400</span><span class="sxs-lookup"><span data-stu-id="72716-108">Example 1 : Creates a new Azure healthcareapis fhir service named MyService in the resource group MyResourceGroup in a location westus2 with cosmosdb offer throughput = 400</span></span>
```powershell
PS C:\> New-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup -Location MyLocation -Kind fhir-R4 -CosmosOfferThroughput  400

ResourceGroupName Name Location        Kind   CosmosOfferThroughput
----------------- ----------- -------------------------------
MyResourceGroup   MyService   westus2    fhir-R4   400

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbOfferThroughput : 400
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

## <span data-ttu-id="72716-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="72716-109">PARAMETERS</span></span>

### <span data-ttu-id="72716-110">-AccessPolicyObjectId</span><span class="sxs-lookup"><span data-stu-id="72716-110">-AccessPolicyObjectId</span></span>
<span data-ttu-id="72716-111">Lista över objekt-ID: n för Access policy.</span><span class="sxs-lookup"><span data-stu-id="72716-111">List of Access Policy Object IDs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72716-112">-AllowCorsCredential</span><span class="sxs-lookup"><span data-stu-id="72716-112">-AllowCorsCredential</span></span>
<span data-ttu-id="72716-113">HealthcareApis FHIR tjänst AllowCorsCredential.</span><span class="sxs-lookup"><span data-stu-id="72716-113">HealthcareApis Fhir Service AllowCorsCredential.</span></span>

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

### <span data-ttu-id="72716-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="72716-114">-AsJob</span></span>
<span data-ttu-id="72716-115">Kör cmdlet som ett jobb i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="72716-115">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="72716-116">-Åhörare</span><span class="sxs-lookup"><span data-stu-id="72716-116">-Audience</span></span>
<span data-ttu-id="72716-117">HealthcareApis FHIR tjänstens mål grupp.</span><span class="sxs-lookup"><span data-stu-id="72716-117">HealthcareApis Fhir Service Audience.</span></span>

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

### <span data-ttu-id="72716-118">-Myndighet</span><span class="sxs-lookup"><span data-stu-id="72716-118">-Authority</span></span>
<span data-ttu-id="72716-119">HealthcareApis FHIR tjänst utfärdare.</span><span class="sxs-lookup"><span data-stu-id="72716-119">HealthcareApis Fhir Service Authority.</span></span>

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

### <span data-ttu-id="72716-120">-CorsHeader</span><span class="sxs-lookup"><span data-stu-id="72716-120">-CorsHeader</span></span>
<span data-ttu-id="72716-121">HealthcareApis FHIR tjänst lista över CORS-rubriker.</span><span class="sxs-lookup"><span data-stu-id="72716-121">HealthcareApis Fhir Service List of Cors Header.</span></span> <span data-ttu-id="72716-122">Ange HTTP-huvuden som kan användas under begäran.</span><span class="sxs-lookup"><span data-stu-id="72716-122">Specify HTTP headers which can be used during the request.</span></span> <span data-ttu-id="72716-123">Använd \* för alla sidhuvuden.</span><span class="sxs-lookup"><span data-stu-id="72716-123">Use \* for any header.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72716-124">-CorsMaxAge</span><span class="sxs-lookup"><span data-stu-id="72716-124">-CorsMaxAge</span></span>
<span data-ttu-id="72716-125">HealthcareApis FHIR tjänst CORS Max åldern.</span><span class="sxs-lookup"><span data-stu-id="72716-125">HealthcareApis Fhir Service Cors Max Age.</span></span> <span data-ttu-id="72716-126">Ange hur lång tid ett resultat från en begäran kan cachelagras på några sekunder.</span><span class="sxs-lookup"><span data-stu-id="72716-126">Specify how long a result from a request can be cached in seconds.</span></span> <span data-ttu-id="72716-127">Exempel: 600 betyder 10 minuter.</span><span class="sxs-lookup"><span data-stu-id="72716-127">Example: 600 means 10 minutes.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72716-128">-CorsMethod</span><span class="sxs-lookup"><span data-stu-id="72716-128">-CorsMethod</span></span>
<span data-ttu-id="72716-129">HealthcareApis FHIR-tjänsten lista över CORS-metod.</span><span class="sxs-lookup"><span data-stu-id="72716-129">HealthcareApis Fhir Service List of Cors Method.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72716-130">-CorsOrigin</span><span class="sxs-lookup"><span data-stu-id="72716-130">-CorsOrigin</span></span>
<span data-ttu-id="72716-131">HealthcareApis FHIR tjänst lista över CORS Origine.</span><span class="sxs-lookup"><span data-stu-id="72716-131">HealthcareApis Fhir Service List of Cors Origin.</span></span> <span data-ttu-id="72716-132">Ange URL: er för ursprungs webbplatser som har till gång till detta API eller Använd \* för att tillåta åtkomst från vilken webbplats som helst.</span><span class="sxs-lookup"><span data-stu-id="72716-132">Specify URLs of origin sites that can access this API, or use \* to allow access from any site.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72716-133">-CosmosOfferThroughput</span><span class="sxs-lookup"><span data-stu-id="72716-133">-CosmosOfferThroughput</span></span>
<span data-ttu-id="72716-134">HealthcareApis FHIR tjänst CosmosOfferThroughput.</span><span class="sxs-lookup"><span data-stu-id="72716-134">HealthcareApis Fhir Service CosmosOfferThroughput.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72716-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72716-135">-DefaultProfile</span></span>
<span data-ttu-id="72716-136">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="72716-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72716-137">-EnableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="72716-137">-EnableSmartProxy</span></span>
<span data-ttu-id="72716-138">HealthcareApis FHIR tjänst EnableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="72716-138">HealthcareApis Fhir Service EnableSmartProxy.</span></span>

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

### <span data-ttu-id="72716-139">-ExportStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="72716-139">-ExportStorageAccountName</span></span>
<span data-ttu-id="72716-140">HealthcareApis FHIR.</span><span class="sxs-lookup"><span data-stu-id="72716-140">HealthcareApis Fhir Service Export Storage Account Name.</span></span>

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

### <span data-ttu-id="72716-141">-FhirVersion</span><span class="sxs-lookup"><span data-stu-id="72716-141">-FhirVersion</span></span>
<span data-ttu-id="72716-142">FHIR-version.</span><span class="sxs-lookup"><span data-stu-id="72716-142">Fhir Version.</span></span>

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

### <span data-ttu-id="72716-143">-Sort</span><span class="sxs-lookup"><span data-stu-id="72716-143">-Kind</span></span>
<span data-ttu-id="72716-144">Typ av HealthcareApis-tjänst.</span><span class="sxs-lookup"><span data-stu-id="72716-144">Kind of HealthcareApis Service.</span></span>
<span data-ttu-id="72716-145">Standardvärdet är FHIR</span><span class="sxs-lookup"><span data-stu-id="72716-145">The default value is Fhir</span></span>

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

### <span data-ttu-id="72716-146">-Plats</span><span class="sxs-lookup"><span data-stu-id="72716-146">-Location</span></span>
<span data-ttu-id="72716-147">HealthcareApis tjänst plats.</span><span class="sxs-lookup"><span data-stu-id="72716-147">HealthcareApis Service Location.</span></span>

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

### <span data-ttu-id="72716-148">-ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="72716-148">-ManagedIdentity</span></span>
<span data-ttu-id="72716-149">Använd hanterad identitet?</span><span class="sxs-lookup"><span data-stu-id="72716-149">Use Managed Identity?</span></span>

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

### <span data-ttu-id="72716-150">-Namn</span><span class="sxs-lookup"><span data-stu-id="72716-150">-Name</span></span>
<span data-ttu-id="72716-151">HealthcareApis-tjänstens namn.</span><span class="sxs-lookup"><span data-stu-id="72716-151">HealthcareApis Service Name.</span></span>

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

### <span data-ttu-id="72716-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72716-152">-ResourceGroupName</span></span>
<span data-ttu-id="72716-153">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="72716-153">Resource Group Name.</span></span>

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

### <span data-ttu-id="72716-154">-Tagg</span><span class="sxs-lookup"><span data-stu-id="72716-154">-Tag</span></span>
<span data-ttu-id="72716-155">HealthcareApis FHIR.</span><span class="sxs-lookup"><span data-stu-id="72716-155">HealthcareApis Fhir Service Account Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72716-156">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="72716-156">-Confirm</span></span>
<span data-ttu-id="72716-157">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="72716-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72716-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72716-158">-WhatIf</span></span>
<span data-ttu-id="72716-159">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="72716-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72716-160">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="72716-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72716-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72716-161">CommonParameters</span></span>
<span data-ttu-id="72716-162">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72716-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72716-163">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="72716-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72716-164">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="72716-164">INPUTS</span></span>

### <span data-ttu-id="72716-165">System. String</span><span class="sxs-lookup"><span data-stu-id="72716-165">System.String</span></span>

## <span data-ttu-id="72716-166">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="72716-166">OUTPUTS</span></span>

### <span data-ttu-id="72716-167">Microsoft. Azure. commands. HealthcareApisService. Models. PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="72716-167">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="72716-168">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="72716-168">NOTES</span></span>

## <span data-ttu-id="72716-169">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="72716-169">RELATED LINKS</span></span>
