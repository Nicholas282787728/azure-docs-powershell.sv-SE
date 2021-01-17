---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/new-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/New-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/New-AzHealthcareApisService.md
ms.openlocfilehash: 33f1af70b0fef7e89ccb584ed3b69f32e2810690
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98415792"
---
# <span data-ttu-id="214fc-101">New-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="214fc-101">New-AzHealthcareApisService</span></span>

## <span data-ttu-id="214fc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="214fc-102">SYNOPSIS</span></span>
<span data-ttu-id="214fc-103">Skapar metadata för en tjänst instans.</span><span class="sxs-lookup"><span data-stu-id="214fc-103">Creates the metadata of a service instance.</span></span>

## <span data-ttu-id="214fc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="214fc-104">SYNTAX</span></span>

```
New-AzHealthcareApisService -Name <String> -ResourceGroupName <String> -Location <String> [-Kind <String>]
 [-AccessPolicyObjectId <String[]>] [-AllowCorsCredential] [-Audience <String>] [-Authority <String>]
 [-CorsHeader <String[]>] [-CorsMaxAge <Int32>] [-CorsMethod <String[]>] [-CorsOrigin <String[]>]
 [-CosmosOfferThroughput <Int32>] [-CosmosKeyVaultKeyUri <String>] [-ExportStorageAccountName <String>]
 [-EnableSmartProxy] [-ManagedIdentity] [-FhirVersion <String>] [-Tag <Hashtable>] [-AsJob]
 [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="214fc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="214fc-105">DESCRIPTION</span></span>
<span data-ttu-id="214fc-106">Skapar eller uppdaterar metadata för en tjänst instans.</span><span class="sxs-lookup"><span data-stu-id="214fc-106">Creates or updates the metadata of a service instance.</span></span>

## <span data-ttu-id="214fc-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="214fc-107">EXAMPLES</span></span>

### <span data-ttu-id="214fc-108">Exempel 1: skapar en ny Azure healthcareapis FHIR-tjänst som heter min tjänst i resurs gruppen MyResourceGroup på en plats westus2 med cosmosdb offer genomflöde = 400</span><span class="sxs-lookup"><span data-stu-id="214fc-108">Example 1 : Creates a new Azure healthcareapis fhir service named MyService in the resource group MyResourceGroup in a location westus2 with cosmosdb offer throughput = 400</span></span>
```powershell
PS C:\> New-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup -Location MyLocation -Kind fhir-R4 -CosmosOfferThroughput 400

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbKeyVaultKeyUri  : 
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

### <span data-ttu-id="214fc-109">Exempel 2: skapar en ny Azure healthcareapis FHIR-tjänst som heter min tjänst i resurs grupps MyResourceGroup på en plats westus2 med cosmosdb offerter = 400 och Key valv Key URI "https:// \<my-keyvault> . Vault.Azure.net/Keys/ \<my-key> "</span><span class="sxs-lookup"><span data-stu-id="214fc-109">Example 2 : Creates a new Azure healthcareapis fhir service named MyService in the resource group MyResourceGroup in a location westus2 with cosmosdb offer throughput = 400 and key vault key uri "https://\<my-keyvault>.vault.azure.net/keys/\<my-key>"</span></span>
```powershell
PS C:\> New-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup -Location MyLocation -Kind fhir-R4 -CosmosOfferThroughput 400 -CosmosKeyVaultKeyUri "https://<my-keyvault>.vault.azure.net/keys/<my-key>"

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbKeyVaultKeyUri  : https://<my-keyvault>.vault.azure.net/keys/<my-key>
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

## <span data-ttu-id="214fc-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="214fc-110">PARAMETERS</span></span>

### <span data-ttu-id="214fc-111">-AccessPolicyObjectId</span><span class="sxs-lookup"><span data-stu-id="214fc-111">-AccessPolicyObjectId</span></span>
<span data-ttu-id="214fc-112">Lista över objekt-ID: n för Access policy.</span><span class="sxs-lookup"><span data-stu-id="214fc-112">List of Access Policy Object IDs.</span></span>

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

### <span data-ttu-id="214fc-113">-AllowCorsCredential</span><span class="sxs-lookup"><span data-stu-id="214fc-113">-AllowCorsCredential</span></span>
<span data-ttu-id="214fc-114">HealthcareApis FHIR tjänst AllowCorsCredentials.</span><span class="sxs-lookup"><span data-stu-id="214fc-114">HealthcareApis Fhir Service AllowCorsCredentials.</span></span>

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

### <span data-ttu-id="214fc-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="214fc-115">-AsJob</span></span>
<span data-ttu-id="214fc-116">Kör cmdlet som ett jobb i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="214fc-116">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="214fc-117">-Åhörare</span><span class="sxs-lookup"><span data-stu-id="214fc-117">-Audience</span></span>
<span data-ttu-id="214fc-118">HealthcareApis FHIR tjänstens mål grupp.</span><span class="sxs-lookup"><span data-stu-id="214fc-118">HealthcareApis Fhir Service Audience.</span></span>

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

### <span data-ttu-id="214fc-119">-Myndighet</span><span class="sxs-lookup"><span data-stu-id="214fc-119">-Authority</span></span>
<span data-ttu-id="214fc-120">HealthcareApis FHIR tjänst utfärdare.</span><span class="sxs-lookup"><span data-stu-id="214fc-120">HealthcareApis Fhir Service Authority.</span></span>

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

### <span data-ttu-id="214fc-121">-CorsHeader</span><span class="sxs-lookup"><span data-stu-id="214fc-121">-CorsHeader</span></span>
<span data-ttu-id="214fc-122">HealthcareApis FHIR tjänst lista över CORS-rubriker.</span><span class="sxs-lookup"><span data-stu-id="214fc-122">HealthcareApis Fhir Service List of Cors Header.</span></span>
<span data-ttu-id="214fc-123">Ange HTTP-huvuden som kan användas under begäran.</span><span class="sxs-lookup"><span data-stu-id="214fc-123">Specify HTTP headers which can be used during the request.</span></span>
<span data-ttu-id="214fc-124">Använd "\*" för alla rubriker.</span><span class="sxs-lookup"><span data-stu-id="214fc-124">Use " \* " for any header.</span></span>

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

### <span data-ttu-id="214fc-125">-CorsMaxAge</span><span class="sxs-lookup"><span data-stu-id="214fc-125">-CorsMaxAge</span></span>
<span data-ttu-id="214fc-126">HealthcareApis FHIR tjänst CORS Max åldern.</span><span class="sxs-lookup"><span data-stu-id="214fc-126">HealthcareApis Fhir Service Cors Max Age.</span></span>
<span data-ttu-id="214fc-127">Ange hur lång tid ett resultat från en begäran kan cachelagras på några sekunder.</span><span class="sxs-lookup"><span data-stu-id="214fc-127">Specify how long a result from a request can be cached in seconds.</span></span>
<span data-ttu-id="214fc-128">Exempel: 600 betyder 10 minuter.</span><span class="sxs-lookup"><span data-stu-id="214fc-128">Example: 600 means 10 minutes.</span></span>

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

### <span data-ttu-id="214fc-129">-CorsMethod</span><span class="sxs-lookup"><span data-stu-id="214fc-129">-CorsMethod</span></span>
<span data-ttu-id="214fc-130">HealthcareApis FHIR-tjänsten lista över CORS-metod.</span><span class="sxs-lookup"><span data-stu-id="214fc-130">HealthcareApis Fhir Service List of Cors Method.</span></span>

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

### <span data-ttu-id="214fc-131">-CorsOrigin</span><span class="sxs-lookup"><span data-stu-id="214fc-131">-CorsOrigin</span></span>
<span data-ttu-id="214fc-132">HealthcareApis FHIR tjänst lista över CORS Origine.</span><span class="sxs-lookup"><span data-stu-id="214fc-132">HealthcareApis Fhir Service List of Cors Origin.</span></span>
<span data-ttu-id="214fc-133">Ange URL: er för ursprungs webbplatser som har åtkomst till detta API eller Använd "\*" för att tillåta åtkomst från vilken webbplats som helst.</span><span class="sxs-lookup"><span data-stu-id="214fc-133">Specify URLs of origin sites that can access this API, or use " \* " to allow access from any site.</span></span>

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

### <span data-ttu-id="214fc-134">-CosmosKeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="214fc-134">-CosmosKeyVaultKeyUri</span></span>
<span data-ttu-id="214fc-135">HealthcareApis FHIR tjänst CosmosKeyVaultKeyUri.</span><span class="sxs-lookup"><span data-stu-id="214fc-135">HealthcareApis Fhir Service CosmosKeyVaultKeyUri.</span></span>
<span data-ttu-id="214fc-136">URI för den Kundhanterade säkerhets knappen för den säkerhetskopierade databasen.</span><span class="sxs-lookup"><span data-stu-id="214fc-136">The URI of the customer-managed key for the backing database.</span></span>

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

### <span data-ttu-id="214fc-137">-CosmosOfferThroughput</span><span class="sxs-lookup"><span data-stu-id="214fc-137">-CosmosOfferThroughput</span></span>
<span data-ttu-id="214fc-138">HealthcareApis FHIR tjänst CosmosOfferThroughput.</span><span class="sxs-lookup"><span data-stu-id="214fc-138">HealthcareApis Fhir Service CosmosOfferThroughput.</span></span>

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

### <span data-ttu-id="214fc-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="214fc-139">-DefaultProfile</span></span>
<span data-ttu-id="214fc-140">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="214fc-140">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="214fc-141">-EnableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="214fc-141">-EnableSmartProxy</span></span>
<span data-ttu-id="214fc-142">HealthcareApis FHIR tjänst EnableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="214fc-142">HealthcareApis Fhir Service EnableSmartProxy.</span></span>

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

### <span data-ttu-id="214fc-143">-ExportStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="214fc-143">-ExportStorageAccountName</span></span>
<span data-ttu-id="214fc-144">HealthcareApis FHIR.</span><span class="sxs-lookup"><span data-stu-id="214fc-144">HealthcareApis Fhir Service Export Storage Account Name.</span></span>

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

### <span data-ttu-id="214fc-145">-FhirVersion</span><span class="sxs-lookup"><span data-stu-id="214fc-145">-FhirVersion</span></span>
<span data-ttu-id="214fc-146">FHIR-version.</span><span class="sxs-lookup"><span data-stu-id="214fc-146">Fhir Version.</span></span>

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

### <span data-ttu-id="214fc-147">-Sort</span><span class="sxs-lookup"><span data-stu-id="214fc-147">-Kind</span></span>
<span data-ttu-id="214fc-148">Typ av HealthcareApis-tjänst.</span><span class="sxs-lookup"><span data-stu-id="214fc-148">Kind of HealthcareApis Service.</span></span>
<span data-ttu-id="214fc-149">Standardvärdet är FHIR</span><span class="sxs-lookup"><span data-stu-id="214fc-149">The default value is Fhir</span></span>

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

### <span data-ttu-id="214fc-150">-Plats</span><span class="sxs-lookup"><span data-stu-id="214fc-150">-Location</span></span>
<span data-ttu-id="214fc-151">HealthcareApis tjänst plats.</span><span class="sxs-lookup"><span data-stu-id="214fc-151">HealthcareApis Service Location.</span></span>

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

### <span data-ttu-id="214fc-152">-ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="214fc-152">-ManagedIdentity</span></span>
<span data-ttu-id="214fc-153">Använd hanterad identitet?</span><span class="sxs-lookup"><span data-stu-id="214fc-153">Use Managed Identity?</span></span>

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

### <span data-ttu-id="214fc-154">-Namn</span><span class="sxs-lookup"><span data-stu-id="214fc-154">-Name</span></span>
<span data-ttu-id="214fc-155">HealthcareApis-tjänstens namn.</span><span class="sxs-lookup"><span data-stu-id="214fc-155">HealthcareApis Service Name.</span></span>

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

### <span data-ttu-id="214fc-156">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="214fc-156">-PublicNetworkAccess</span></span>
<span data-ttu-id="214fc-157">Nätverks åtkomst typen för FHIR-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="214fc-157">The network access type for Fhir service.</span></span> <span data-ttu-id="214fc-158">Vanligt vis `Enabled` eller `Disabled` .</span><span class="sxs-lookup"><span data-stu-id="214fc-158">Commonly `Enabled` or `Disabled`.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="214fc-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="214fc-159">-ResourceGroupName</span></span>
<span data-ttu-id="214fc-160">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="214fc-160">Resource Group Name.</span></span>

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

### <span data-ttu-id="214fc-161">-Tagg</span><span class="sxs-lookup"><span data-stu-id="214fc-161">-Tag</span></span>
<span data-ttu-id="214fc-162">HealthcareApis FHIR.</span><span class="sxs-lookup"><span data-stu-id="214fc-162">HealthcareApis Fhir Service Account Tags.</span></span>

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

### <span data-ttu-id="214fc-163">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="214fc-163">-Confirm</span></span>
<span data-ttu-id="214fc-164">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="214fc-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="214fc-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="214fc-165">-WhatIf</span></span>
<span data-ttu-id="214fc-166">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="214fc-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="214fc-167">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="214fc-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="214fc-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="214fc-168">CommonParameters</span></span>
<span data-ttu-id="214fc-169">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="214fc-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="214fc-170">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="214fc-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="214fc-171">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="214fc-171">INPUTS</span></span>

### <span data-ttu-id="214fc-172">System. String</span><span class="sxs-lookup"><span data-stu-id="214fc-172">System.String</span></span>

## <span data-ttu-id="214fc-173">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="214fc-173">OUTPUTS</span></span>

### <span data-ttu-id="214fc-174">Microsoft. Azure. commands. HealthcareApis. Models. PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="214fc-174">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="214fc-175">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="214fc-175">NOTES</span></span>

## <span data-ttu-id="214fc-176">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="214fc-176">RELATED LINKS</span></span>
