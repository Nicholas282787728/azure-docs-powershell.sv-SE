---
ms.openlocfilehash: 911e1f7ff56feab2735f397a0128aab4aa7757c7
ms.sourcegitcommit: 0c012450805bef75472f48c74fe488baf6ba53bb
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/04/2019
ms.locfileid: "66498683"
---
## <a name="220---june-2019"></a><span data-ttu-id="09d17-101">2.2.0 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="09d17-101">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="09d17-102">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="09d17-102">Az.Cdn</span></span>
* <span data-ttu-id="09d17-103">Uppdaterade cmdletar för att ge stöd för rulesEngine-funktion baserat på API-version 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="09d17-103">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="09d17-104">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="09d17-104">Az.Compute</span></span>
* <span data-ttu-id="09d17-105">Lade till parameter `NoWait` som startar åtgärden och returnerar omedelbart, innan åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="09d17-105">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="09d17-106">Uppdaterade cmdletar:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="09d17-106">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="09d17-107">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="09d17-107">Az.EventHub</span></span>
* <span data-ttu-id="09d17-108">Korrigering för #9231 – Get-AzEventHubNamespace returnerar inga taggar</span><span class="sxs-lookup"><span data-stu-id="09d17-108">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="09d17-109">Korrigering för #9230 – Get-AzEventHubNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09d17-109">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="09d17-110">Az.Network</span><span class="sxs-lookup"><span data-stu-id="09d17-110">Az.Network</span></span>
* <span data-ttu-id="09d17-111">Uppdatera ResourceId och InputObject för NAT-gateway</span><span class="sxs-lookup"><span data-stu-id="09d17-111">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="09d17-112">Lägg till alias för ResourceId och InputObject</span><span class="sxs-lookup"><span data-stu-id="09d17-112">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="09d17-113">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="09d17-113">Az.PolicyInsights</span></span>
* <span data-ttu-id="09d17-114">Åtgärda Null-referensproblem i Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="09d17-114">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="09d17-115">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="09d17-115">Az.RecoveryServices</span></span>
* <span data-ttu-id="09d17-116">Minsta kvarhållning för IaaSVM-policy i dagar ändrat till 7 från 1</span><span class="sxs-lookup"><span data-stu-id="09d17-116">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="09d17-117">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="09d17-117">Az.ServiceBus</span></span>
* <span data-ttu-id="09d17-118">Korrigering för ärende #9182 – Get-AzServiceBusNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09d17-118">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="09d17-119">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="09d17-119">Az.ServiceFabric</span></span>
* <span data-ttu-id="09d17-120">Åtgärda stavfel i felmeddelandet för Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="09d17-120">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="09d17-121">Åtgärda saknat tecken i Service Fabric-kommandorader</span><span class="sxs-lookup"><span data-stu-id="09d17-121">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="09d17-122">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="09d17-122">Az.Sql</span></span>
* <span data-ttu-id="09d17-123">Lägg till parametern DnsZonePartner för New-AzureSqlInstance-cmdlet för att ge stöd för AutoDr för hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="09d17-123">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="09d17-124">Avvecklar cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="09d17-124">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="09d17-125">Döp om cmdletar för hotidentifiering till Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="09d17-125">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="09d17-126">Parametrarna New-AzSqlInstance -StorageSizeInGB och -LicenseType är nu valfria.</span><span class="sxs-lookup"><span data-stu-id="09d17-126">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="09d17-127">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="09d17-127">Az.Websites</span></span>
* <span data-ttu-id="09d17-128">åtgärdar problemet där användningen av Set-AzWebApp och Set-AzWebAppSlot med -WebApp-egenskap tog bort taggarna</span><span class="sxs-lookup"><span data-stu-id="09d17-128">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="09d17-129">2.1.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="09d17-129">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="09d17-130">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="09d17-130">Az.ApiManagement</span></span>
* <span data-ttu-id="09d17-131">Skapade nya cmdletar för att hantera diagnostik för global- och API-omfång</span><span class="sxs-lookup"><span data-stu-id="09d17-131">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="09d17-132">**Get-AzApiManagementDiagnostic** – Skaffa diagnostik konfigurerad för global- eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="09d17-132">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="09d17-133">**New-AzApiManagementDiagnostic** – Skapa ny diagnostik för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="09d17-133">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="09d17-134">**New-AzApiManagementHttpMessageDiagnostic** – Skapa diagnostikinställning om vilka rubriker som ska loggas och storleken på brödtextbyte</span><span class="sxs-lookup"><span data-stu-id="09d17-134">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="09d17-135">**New-AzApiManagementPipelineDiagnosticSetting** – Skapa diagnostikinställningar för inkommande/utgående HTTP-meddelanden till gatewayen.</span><span class="sxs-lookup"><span data-stu-id="09d17-135">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="09d17-136">**New-AzApiManagementSamplingSetting** – Skapa samplinginställningar för begäranden/svar för en diagnostik</span><span class="sxs-lookup"><span data-stu-id="09d17-136">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="09d17-137">**Remove-AzApiManagementDiagnostic** – Ta bort en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="09d17-137">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="09d17-138">**Set-AzApiManagementDiagnostic** – Uppdatera en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="09d17-138">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="09d17-139">Skapade nya cmdletar för hantering av cacheminne i ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="09d17-139">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="09d17-140">**Get-AzApiManagementCache** – Hämta information om cacheminnet som anges av identifierare eller alla cacheminnen</span><span class="sxs-lookup"><span data-stu-id="09d17-140">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="09d17-141">**New-AzApiManagementCache** – Skapa ett nytt default-cacheminne eller cacheminne i en viss Azure-region</span><span class="sxs-lookup"><span data-stu-id="09d17-141">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="09d17-142">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="09d17-142">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="09d17-143">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="09d17-143">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="09d17-144">Skapade nya cmdletar för hantering av API-schema</span><span class="sxs-lookup"><span data-stu-id="09d17-144">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="09d17-145">**New-AzApiManagementSchema** – Skapa ett nytt schema för ett API</span><span class="sxs-lookup"><span data-stu-id="09d17-145">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="09d17-146">**Get-AzApiManagementSchema** – Hämta de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="09d17-146">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="09d17-147">**Remove-AzApiManagementSchema** – Ta bort de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="09d17-147">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="09d17-148">**Set-AzApiManagementSchema** – Uppdatera de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="09d17-148">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="09d17-149">Skapa ny cmdlet för att generera en användartoken.</span><span class="sxs-lookup"><span data-stu-id="09d17-149">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="09d17-150">**New-AzApiManagementUserToken** – Skapa en ny användartoken som enligt standardinställning är giltig i 8 timmar. Token för GIT-användaren kan skapas med den här cmdleten./</span><span class="sxs-lookup"><span data-stu-id="09d17-150">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="09d17-151">Skapade en ny cmdlet för att hämta nätverksstatus</span><span class="sxs-lookup"><span data-stu-id="09d17-151">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="09d17-152">**Get-AzApiManagementNetworkStatus** – Hämta nätverksstatusanslutningen för resurserna som API Management-tjänsten är beroende av.</span><span class="sxs-lookup"><span data-stu-id="09d17-152">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="09d17-153">Det här är användbart när du distribuerar ApiManagement-tjänsten i ett virtuellt nätverk och validerar om något beroende är brutet.</span><span class="sxs-lookup"><span data-stu-id="09d17-153">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="09d17-154">Uppdaterade cmdlet **New-AzApiManagement** för att hantera ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="09d17-154">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="09d17-155">Lade till stöd för den nya SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="09d17-155">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="09d17-156">Aktiverade stöd för att slå på flaggan EnableClientCertificate för SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="09d17-156">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="09d17-157">Den nya cmdleten **New-AzApiManagementSslSetting** gör det möjligt att ställa in TLS/SSL-inställningen på ”Backend” och ”Frontend” (serverdel och klientdel).</span><span class="sxs-lookup"><span data-stu-id="09d17-157">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="09d17-158">Det här kan också användas till att konfigurera chiffer som 3DES och ServerProtocols som Http2 för Frontend för en ApiManagement-tjänst.</span><span class="sxs-lookup"><span data-stu-id="09d17-158">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="09d17-159">Stöd har lagts till för att konfigurera värdnamnet DeveloperPortal på ApiManagement-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="09d17-159">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="09d17-160">Uppdaterade cmdletar **Get-AzApiManagementSsoToken** för att ta PsApiManagement-objekt som indata</span><span class="sxs-lookup"><span data-stu-id="09d17-160">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="09d17-161">Uppdaterad cmdleten för att visa infogade felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="09d17-161">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="09d17-162">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Felkod: Felmeddelande av typen ValidationError: Ett eller flera fält innehåller felaktiga värden: Felinformation:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="09d17-162">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="09d17-163">Uppdaterade cmdlet **Export-AzApiManagementApi** för att exportera API:er i OpenApi 3.0-format</span><span class="sxs-lookup"><span data-stu-id="09d17-163">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="09d17-164">Uppdaterade cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="09d17-164">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="09d17-165">Importera API från dokumentspecifikationen OpenApi 3.0</span><span class="sxs-lookup"><span data-stu-id="09d17-165">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="09d17-166">Om du vill åsidosätta egenskapen PsApiManagementSchema specificerad i ett dokument (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="09d17-166">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="09d17-167">Åsidosätta egenskapen ServiceUrl som specificeras i ett dokument.</span><span class="sxs-lookup"><span data-stu-id="09d17-167">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="09d17-168">Uppdaterade cmdlet **Get-AzApiManagementPolicy** för att returnera policy i undantaget format av typen icke-XML med rawxml</span><span class="sxs-lookup"><span data-stu-id="09d17-168">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="09d17-169">Uppdaterade cmdlet **Set-AzApiManagementPolicy** för att godkänna policy i undantaget format av typen icke-XML med rawxml och XML undantaget med xml</span><span class="sxs-lookup"><span data-stu-id="09d17-169">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="09d17-170">Uppdaterad cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="09d17-170">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="09d17-171">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="09d17-171">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="09d17-172">Skapa ett API i ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="09d17-172">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="09d17-173">Klona ett API med SourceApiId och SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="09d17-173">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="09d17-174">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="09d17-174">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="09d17-175">Uppdaterad cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="09d17-175">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="09d17-176">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="09d17-176">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="09d17-177">Uppdatera ett API till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="09d17-177">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="09d17-178">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="09d17-178">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="09d17-179">Uppdaterad cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="09d17-179">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="09d17-180">Klona en befintlig version med hjälp av SourceApiRevision (kopiera taggar, produkter, åtgärder och principer).</span><span class="sxs-lookup"><span data-stu-id="09d17-180">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="09d17-181">Den nya revisionen antar ApiId från den överordnade instansen.</span><span class="sxs-lookup"><span data-stu-id="09d17-181">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="09d17-182">Tillhandahålla ApiRevisionDescription</span><span class="sxs-lookup"><span data-stu-id="09d17-182">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="09d17-183">Åsidosätta ServiceUrl vid kloning av ett API.</span><span class="sxs-lookup"><span data-stu-id="09d17-183">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="09d17-184">Uppdaterad cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="09d17-184">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="09d17-185">Konfigurera AAD eller AADB2C med en Authority</span><span class="sxs-lookup"><span data-stu-id="09d17-185">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="09d17-186">Konfigurera SignupPolicy, SigninPolicy, ProfileEditingPolicy och PasswordResetPolicy</span><span class="sxs-lookup"><span data-stu-id="09d17-186">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="09d17-187">Uppdaterad cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="09d17-187">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="09d17-188">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="09d17-188">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="09d17-189">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="09d17-189">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="09d17-190">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="09d17-190">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="09d17-191">Uppdaterad cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="09d17-191">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="09d17-192">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="09d17-192">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="09d17-193">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="09d17-193">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="09d17-194">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="09d17-194">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="09d17-195">Uppdaterade följande cmdletar för att acceptera ResourceId som indata</span><span class="sxs-lookup"><span data-stu-id="09d17-195">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="09d17-196">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="09d17-196">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="09d17-197">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="09d17-197">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="09d17-198">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="09d17-198">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="09d17-199">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="09d17-199">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="09d17-200">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="09d17-200">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="09d17-201">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="09d17-201">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="09d17-202">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="09d17-202">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="09d17-203">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="09d17-203">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="09d17-204">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="09d17-204">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="09d17-205">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="09d17-205">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="09d17-206">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="09d17-206">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="09d17-207">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="09d17-207">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="09d17-208">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="09d17-208">Az.Automation</span></span>
* <span data-ttu-id="09d17-209">Uppdaterade Get-AzAutomationJobOutputRecord för att hantera postvärden av typen JSON och Text.</span><span class="sxs-lookup"><span data-stu-id="09d17-209">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="09d17-210">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="09d17-210">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="09d17-211">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="09d17-211">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="09d17-212">Ändrade beteende för Start-AzAutomationDscCompilationJob till att bara starta jobbet istället för att vänta på slutförandet.</span><span class="sxs-lookup"><span data-stu-id="09d17-212">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="09d17-213">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="09d17-213">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="09d17-214">Korrigering för Get-AzAutomationDscNode när using -Name returnerar alla noder.</span><span class="sxs-lookup"><span data-stu-id="09d17-214">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="09d17-215">Nu returnerar den endast den matchande noden.</span><span class="sxs-lookup"><span data-stu-id="09d17-215">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="09d17-216">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="09d17-216">Az.Compute</span></span>
* <span data-ttu-id="09d17-217">Lägg till parametrarna ProtectFromScaleIn och ProtectFromScaleSetAction i cmdleten Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="09d17-217">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="09d17-218">Nu är standardinställningen att vimpelparametern New-AzVM använder en tillgänglig plats om USA, östra inte stöds</span><span class="sxs-lookup"><span data-stu-id="09d17-218">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="09d17-219">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="09d17-219">Az.DataLakeStore</span></span>
* <span data-ttu-id="09d17-220">Uppdatera ADLS-sdk för att använda httpclient, integrera dataplanstestning med Azure-ramverk</span><span class="sxs-lookup"><span data-stu-id="09d17-220">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="09d17-221">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="09d17-221">Az.Monitor</span></span>
* <span data-ttu-id="09d17-222">Korrigera felaktiga parameternamn i hjälpexempel</span><span class="sxs-lookup"><span data-stu-id="09d17-222">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="09d17-223">Az.Network</span><span class="sxs-lookup"><span data-stu-id="09d17-223">Az.Network</span></span>
* <span data-ttu-id="09d17-224">Lägg till flaggan DisableBgpRoutePropagation i utdata för effektiv routningstabell</span><span class="sxs-lookup"><span data-stu-id="09d17-224">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="09d17-225">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="09d17-225">Updated cmdlet:</span></span>
        - <span data-ttu-id="09d17-226">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="09d17-226">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="09d17-227">Åtgärda dubbelstreck i dokumentationen New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="09d17-227">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="09d17-228">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="09d17-228">Az.Resources</span></span>
* <span data-ttu-id="09d17-229">Lägg till ny cmdlet Get-AzureRmDenyAssignment för att hämta tilldelningsnekanden</span><span class="sxs-lookup"><span data-stu-id="09d17-229">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="09d17-230">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="09d17-230">Az.Sql</span></span>
* <span data-ttu-id="09d17-231">Döp om Advanced Threat Protection-cmdletar för Advanced Data Security och aktivera Vulnerability Assessment som standard</span><span class="sxs-lookup"><span data-stu-id="09d17-231">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="09d17-232">2.0.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="09d17-232">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="09d17-233">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="09d17-233">Az.Accounts</span></span>
* <span data-ttu-id="09d17-234">Uppdatera autentiseringsbiblioteket för att åtgärda ADFS-problem med autentisering av användarnamn/lösenord</span><span class="sxs-lookup"><span data-stu-id="09d17-234">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="09d17-235">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="09d17-235">Az.CognitiveServices</span></span>
* <span data-ttu-id="09d17-236">Visa endast Bing-ansvarsfriskrivning för Bing-sökningstjänster.</span><span class="sxs-lookup"><span data-stu-id="09d17-236">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="09d17-237">Förbättra felmeddelande när det inte går att skapa konton.</span><span class="sxs-lookup"><span data-stu-id="09d17-237">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="09d17-238">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="09d17-238">Az.Compute</span></span>
* <span data-ttu-id="09d17-239">Funktion för närhetsplaceringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="09d17-239">Proximity placement group feature.</span></span>
    - <span data-ttu-id="09d17-240">Följande nya cmdletar har lagts till:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="09d17-240">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="09d17-241">Den nya parametern ProximityPlacementGroupId har lagts till i följande cmdletar:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="09d17-241">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="09d17-242">Parametern StorageAccountType har lagts till i New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="09d17-242">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="09d17-243">TargetRegion för New-AzGalleryImageVersion kan innehålla StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="09d17-243">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="09d17-244">Växlingsparametern SkipShutdown har lagts till i Stop-AzVM och Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="09d17-244">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="09d17-245">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="09d17-245">Breaking changes</span></span>
    - <span data-ttu-id="09d17-246">Set-AzVMBootDiagnostics har ändrats till Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="09d17-246">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="09d17-247">Export-AzLogAnalyticThrottledRequests har ändrats till Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="09d17-247">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="09d17-248">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="09d17-248">Az.DeploymentManager</span></span>
* <span data-ttu-id="09d17-249">De första allmänt tillgängliga versionerna av cmdletar för Distributionshanteraren i Azure</span><span class="sxs-lookup"><span data-stu-id="09d17-249">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="09d17-250">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="09d17-250">Az.Dns</span></span>
* <span data-ttu-id="09d17-251">Automatisk delegering av DNS för NameServer</span><span class="sxs-lookup"><span data-stu-id="09d17-251">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="09d17-252">Det överordnade zonnamnet kan användas som ytterligare valfri parameter i cmdleten för att skapa DNS-zoner.</span><span class="sxs-lookup"><span data-stu-id="09d17-252">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="09d17-253">Lägger till NS-poster för en nyligen skapad underordnad zon i den överordnade zonen.</span><span class="sxs-lookup"><span data-stu-id="09d17-253">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="09d17-254">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="09d17-254">Az.FrontDoor</span></span>
* <span data-ttu-id="09d17-255">De första allmänt tillgängliga versionerna av cmdletar för Azure FrontDoor</span><span class="sxs-lookup"><span data-stu-id="09d17-255">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="09d17-256">Byt namn på WAF-cmdletar så att de omfattar ”Waf”</span><span class="sxs-lookup"><span data-stu-id="09d17-256">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="09d17-257">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="09d17-257">Az.HDInsight</span></span>
* <span data-ttu-id="09d17-258">Två cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="09d17-258">Removed two cmdlets:</span></span>
    - <span data-ttu-id="09d17-259">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="09d17-259">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="09d17-260">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="09d17-260">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="09d17-261">En ny cmdlet har lagts till, Set-AzHDInsightGatewayCredential, som ersätter Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="09d17-261">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="09d17-262">Uppdatera cmdleten Get-AzHDInsightJobOutput för att skilja mellan läsarrollen och HDInsight-operatörsrollen:</span><span class="sxs-lookup"><span data-stu-id="09d17-262">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="09d17-263">Användare med läsarrollen måste uttryckligen ange parametern ”DefaultStorageAccountKey”, annars uppstår fel.</span><span class="sxs-lookup"><span data-stu-id="09d17-263">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="09d17-264">Användare med HDInsight-operatörsrollen påverkas inte.</span><span class="sxs-lookup"><span data-stu-id="09d17-264">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="09d17-265">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="09d17-265">Az.Monitor</span></span>
* <span data-ttu-id="09d17-266">Nya cmdletar för SQR API (schemalagd frågeregel)</span><span class="sxs-lookup"><span data-stu-id="09d17-266">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="09d17-267">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="09d17-267">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="09d17-268">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="09d17-268">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="09d17-269">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="09d17-269">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="09d17-270">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="09d17-270">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="09d17-271">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="09d17-271">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="09d17-272">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="09d17-272">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="09d17-273">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="09d17-273">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="09d17-274">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="09d17-274">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="09d17-275">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="09d17-275">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="09d17-276">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="09d17-276">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="09d17-277">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="09d17-277">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="09d17-278">[Mer](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) information om SQR API</span><span class="sxs-lookup"><span data-stu-id="09d17-278">[More](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="09d17-279">Az.Monitor.md har uppdaterats för att omfatta cmdletar för måttbaserade aviseringsregler i GenV2 (inte klassiska)</span><span class="sxs-lookup"><span data-stu-id="09d17-279">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="09d17-280">Az.Network</span><span class="sxs-lookup"><span data-stu-id="09d17-280">Az.Network</span></span>
* <span data-ttu-id="09d17-281">Lägg till stöd för NAT Gateway-resurs</span><span class="sxs-lookup"><span data-stu-id="09d17-281">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="09d17-282">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="09d17-282">New cmdlets</span></span>
        - <span data-ttu-id="09d17-283">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="09d17-283">New-AzNatGateway</span></span>
        - <span data-ttu-id="09d17-284">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="09d17-284">Get-AzNatGateway</span></span>
        - <span data-ttu-id="09d17-285">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="09d17-285">Set-AzNatGateway</span></span>
        - <span data-ttu-id="09d17-286">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="09d17-286">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="09d17-287">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="09d17-287">Updated cmdlets</span></span>
        - <span data-ttu-id="09d17-288">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="09d17-288">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="09d17-289">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="09d17-289">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="09d17-290">Nedanstående kommandon för funktionen har uppdaterats: Ange/ta bort anpassade vägar på Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="09d17-290">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="09d17-291">New-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ställa in adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="09d17-291">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="09d17-292">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ange adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="09d17-292">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="09d17-293">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="09d17-293">Az.PolicyInsights</span></span>
* <span data-ttu-id="09d17-294">Stöd för att fråga efter information om principutvärdering.</span><span class="sxs-lookup"><span data-stu-id="09d17-294">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="09d17-295">Lägg till parametern ”-Expand” för Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="09d17-295">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="09d17-296">Stöd för -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="09d17-296">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="09d17-297">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="09d17-297">Az.RecoveryServices</span></span>
* <span data-ttu-id="09d17-298">Stöd för att dela prenumeration mellan Azure och Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="09d17-298">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="09d17-299">Markering av kommande icke-bakåtkompatibla ändringar för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="09d17-299">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="09d17-300">Korrigering för återställningsplan och åtgärdsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="09d17-300">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="09d17-301">Korrigering för mappning av uppdateringsnätverk i Azure Site Recovery för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="09d17-301">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="09d17-302">Korrigering för instruktioner för uppdateringsskydd i Azure Site Recovery för Azure till Azure för hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="09d17-302">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="09d17-303">Andra mindre korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="09d17-303">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="09d17-304">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="09d17-304">Az.Relay</span></span>
* <span data-ttu-id="09d17-305">Korrigera stavfel i kundriktade meddelanden</span><span class="sxs-lookup"><span data-stu-id="09d17-305">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="09d17-306">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="09d17-306">Az.ServiceBus</span></span>
* <span data-ttu-id="09d17-307">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="09d17-307">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="09d17-308">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="09d17-308">Az.Storage</span></span>
* <span data-ttu-id="09d17-309">Uppgradera till lagringsklientbiblioteket 10.0.1 (namnområdet för alla objekt från detta SDK ändras från ”Microsoft.WindowsAzure.Storage. *till ”Microsoft.Azure.Storage.* ”)</span><span class="sxs-lookup"><span data-stu-id="09d17-309">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="09d17-310">Uppgradera till Microsoft.Azure.Management.Storage 11.0.0 för att stödja den nya API-versionen 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="09d17-310">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="09d17-311">Standardlagringskontot i Skapa lagringskonto ändras från ”Storage” till ”StorageV2”</span><span class="sxs-lookup"><span data-stu-id="09d17-311">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="09d17-312">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="09d17-312">New-AzStorageAccount</span></span>
* <span data-ttu-id="09d17-313">Ändra lagringskontots cmdlet-utdata Sku.Name för att passa med indata-SkuName genom att lägga till ”-”. Till exempel ändras ”StandardLRS” till ”Standard_LRS”</span><span class="sxs-lookup"><span data-stu-id="09d17-313">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="09d17-314">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="09d17-314">New-AzStorageAccount</span></span>
    - <span data-ttu-id="09d17-315">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="09d17-315">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="09d17-316">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="09d17-316">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="09d17-317">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="09d17-317">Az.Websites</span></span>
* <span data-ttu-id="09d17-318">Egenskapen ”typ” konfigureras nu för PSSite-objekt som returneras av Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="09d17-318">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="09d17-319">Get-AzWebApp\*Metrics och Get-AzAppServicePlanMetrics markeras som inaktuella</span><span class="sxs-lookup"><span data-stu-id="09d17-319">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="09d17-320">1.8.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="09d17-320">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="09d17-321">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="09d17-321">Highlights since the last major release</span></span>
* <span data-ttu-id="09d17-322">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="09d17-322">General availability of `Az` module</span></span>
* <span data-ttu-id="09d17-323">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="09d17-323">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="09d17-324">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="09d17-324">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="09d17-325">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="09d17-325">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="09d17-326">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="09d17-326">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="09d17-327">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="09d17-327">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="09d17-328">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="09d17-328">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="09d17-329">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="09d17-329">Az.Accounts</span></span>
* <span data-ttu-id="09d17-330">Uppdatera Uninstall-AzureRm för att ta bort moduler i Mac på ett korrekt sätt</span><span class="sxs-lookup"><span data-stu-id="09d17-330">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="09d17-331">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="09d17-331">Az.Batch</span></span>
* <span data-ttu-id="09d17-332">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="09d17-332">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="09d17-333">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="09d17-333">Az.Cdn</span></span>
* <span data-ttu-id="09d17-334">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="09d17-334">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="09d17-335">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="09d17-335">Az.CognitiveServices</span></span>
* <span data-ttu-id="09d17-336">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="09d17-336">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="09d17-337">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="09d17-337">Az.Compute</span></span>
* <span data-ttu-id="09d17-338">Åtgärda problem med AEM-installationen om resurs-ID:n för diskar innehåller resourcegroups i gemener i resurs-ID:n</span><span class="sxs-lookup"><span data-stu-id="09d17-338">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="09d17-339">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="09d17-339">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="09d17-340">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="09d17-340">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="09d17-341">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="09d17-341">Az.DataFactory</span></span>
* <span data-ttu-id="09d17-342">Lägg till SsisProperties om NodeCount inte är null för hanterad integreringskörning.</span><span class="sxs-lookup"><span data-stu-id="09d17-342">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="09d17-343">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="09d17-343">Az.DataLakeStore</span></span>
* <span data-ttu-id="09d17-344">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="09d17-344">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="09d17-345">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="09d17-345">Az.EventGrid</span></span>
* <span data-ttu-id="09d17-346">Hjälptexten för slutpunkten har uppdaterats för att visa att resurser ska skapas innan cmdletarna för att skapa/uppdatera händelseprenumerationer används.</span><span class="sxs-lookup"><span data-stu-id="09d17-346">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="09d17-347">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="09d17-347">Az.EventHub</span></span>
* <span data-ttu-id="09d17-348">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="09d17-348">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="09d17-349">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="09d17-349">Az.HDInsight</span></span>
* <span data-ttu-id="09d17-350">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="09d17-350">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="09d17-351">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="09d17-351">Az.IotHub</span></span>
* <span data-ttu-id="09d17-352">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="09d17-352">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="09d17-353">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="09d17-353">Az.KeyVault</span></span>
* <span data-ttu-id="09d17-354">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="09d17-354">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="09d17-355">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="09d17-355">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="09d17-356">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="09d17-356">Az.MachineLearning</span></span>
* <span data-ttu-id="09d17-357">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="09d17-357">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="09d17-358">Az.Media</span><span class="sxs-lookup"><span data-stu-id="09d17-358">Az.Media</span></span>
* <span data-ttu-id="09d17-359">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="09d17-359">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="09d17-360">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="09d17-360">Az.Monitor</span></span>
  * <span data-ttu-id="09d17-361">Nya cmdletar för måttbaserad aviseringsregel i GenV2 (inte klassisk)</span><span class="sxs-lookup"><span data-stu-id="09d17-361">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="09d17-362">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="09d17-362">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="09d17-363">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="09d17-363">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="09d17-364">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="09d17-364">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="09d17-365">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="09d17-365">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="09d17-366">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="09d17-366">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="09d17-367">Monitor SDK har uppdaterats till version 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="09d17-367">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="09d17-368">Az.Network</span><span class="sxs-lookup"><span data-stu-id="09d17-368">Az.Network</span></span>
* <span data-ttu-id="09d17-369">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="09d17-369">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="09d17-370">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="09d17-370">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="09d17-371">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="09d17-371">Az.NotificationHubs</span></span>
* <span data-ttu-id="09d17-372">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="09d17-372">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="09d17-373">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="09d17-373">Az.OperationalInsights</span></span>
* <span data-ttu-id="09d17-374">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="09d17-374">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="09d17-375">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="09d17-375">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="09d17-376">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="09d17-376">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="09d17-377">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="09d17-377">Az.RecoveryServices</span></span>
* <span data-ttu-id="09d17-378">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="09d17-378">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="09d17-379">Tabellformatet för SQL i virtuella Azure-datorer har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="09d17-379">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="09d17-380">En alternativ metod för att hämta platser i AzureFileShare har lagts till</span><span class="sxs-lookup"><span data-stu-id="09d17-380">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="09d17-381">ScheduleRunDays i SchedulePolicy-objekt har uppdaterats enligt tidszon</span><span class="sxs-lookup"><span data-stu-id="09d17-381">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="09d17-382">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="09d17-382">Az.RedisCache</span></span>
* <span data-ttu-id="09d17-383">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="09d17-383">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="09d17-384">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="09d17-384">Az.Resources</span></span>
* <span data-ttu-id="09d17-385">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="09d17-385">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="09d17-386">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="09d17-386">Az.Sql</span></span>
* <span data-ttu-id="09d17-387">Ersätt Monitor SDK-beroende med vanlig kod</span><span class="sxs-lookup"><span data-stu-id="09d17-387">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="09d17-388">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="09d17-388">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="09d17-389">Förbättrad process för klassificering av flera kolumner.</span><span class="sxs-lookup"><span data-stu-id="09d17-389">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="09d17-390">Inkludera SKU-egenskaper (SKU-namn, serie, kapacitet) i svaret från Get-AzSqlServerServiceObjective och formatera som tabell som standard.</span><span class="sxs-lookup"><span data-stu-id="09d17-390">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="09d17-391">Möjlighet att använda Get-AzSqlServerServiceObjective efter plats utan att behöva en redan befintlig server i regionen.</span><span class="sxs-lookup"><span data-stu-id="09d17-391">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="09d17-392">Stöd för tidszonsparametern när hanterade instanser skapas.</span><span class="sxs-lookup"><span data-stu-id="09d17-392">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="09d17-393">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="09d17-393">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="09d17-394">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="09d17-394">Az.Websites</span></span>
* <span data-ttu-id="09d17-395">åtgärdar Set-AzWebApp och Set-AzWebAppSlot så att de inte tar bort taggar vid körning</span><span class="sxs-lookup"><span data-stu-id="09d17-395">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="09d17-396">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="09d17-396">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="09d17-397">SDK för WebSites har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="09d17-397">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="09d17-398">Egenskapen AdminSiteName har tagits bort från PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="09d17-398">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="09d17-399">1.7.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="09d17-399">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="09d17-400">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="09d17-400">Highlights since the last major release</span></span>
* <span data-ttu-id="09d17-401">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="09d17-401">General availability of `Az` module</span></span>
* <span data-ttu-id="09d17-402">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="09d17-402">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="09d17-403">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="09d17-403">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="09d17-404">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="09d17-404">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="09d17-405">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="09d17-405">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="09d17-406">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="09d17-406">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="09d17-407">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="09d17-407">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="09d17-408">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="09d17-408">Az.Accounts</span></span>
* <span data-ttu-id="09d17-409">Add-AzEnvironment och Set-AzEnvironment har uppdaterats för att godkänna parametern AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="09d17-409">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="09d17-410">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="09d17-410">Az.AnalysisServices</span></span>
* <span data-ttu-id="09d17-411">ServiceClient används i cmdletar för dataplan och den ursprungliga autentiseringslogiken har tagits bort</span><span class="sxs-lookup"><span data-stu-id="09d17-411">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="09d17-412">Add-AzureASAccount används för omslutning av Connect-AzAccount för att undvika en icke-bakåtkompatibel ändring</span><span class="sxs-lookup"><span data-stu-id="09d17-412">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="09d17-413">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="09d17-413">Az.Automation</span></span>
* <span data-ttu-id="09d17-414">Buggen för cmdleten New-AzAutomationSoftwareUpdateConfiguration för inkluderingar har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="09d17-414">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="09d17-415">Nu bör parametern IncludedKbNumber och IncludedPackageNameMask fungera.</span><span class="sxs-lookup"><span data-stu-id="09d17-415">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="09d17-416">Felkorrigering för dynamiska grupper i uppdateringshanteringen för azure automation</span><span class="sxs-lookup"><span data-stu-id="09d17-416">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="09d17-417">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="09d17-417">Az.Compute</span></span>
* <span data-ttu-id="09d17-418">Lägg till parametern HyperVGeneration i New-AzDiskConfig och New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="09d17-418">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="09d17-419">Tillåt att virtuella datorer skapas med galleribilder från andra klientorganisationer.</span><span class="sxs-lookup"><span data-stu-id="09d17-419">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="09d17-420">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="09d17-420">Az.ContainerInstance</span></span>
* <span data-ttu-id="09d17-421">Ett problem har åtgärdats i parametern -Command för New-AzContainerGroup som lade till ett avslutande tomt argument</span><span class="sxs-lookup"><span data-stu-id="09d17-421">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="09d17-422">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="09d17-422">Az.DataFactory</span></span>
* <span data-ttu-id="09d17-423">ADF .Net SDK-versionen har uppdaterats till 3.0.2</span><span class="sxs-lookup"><span data-stu-id="09d17-423">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="09d17-424">Cmdleten Set-AzDataFactoryV2 har uppdaterats med extra parametrar för inställningar som rör RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="09d17-424">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="09d17-425">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="09d17-425">Az.Resources</span></span>
* <span data-ttu-id="09d17-426">Förbättra hanteringen av providrar för Get-AzResource när parametrarna -ResourceId eller -ResourceGroupName, -Name och -ResourceType tillhandahålls</span><span class="sxs-lookup"><span data-stu-id="09d17-426">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="09d17-427">Förbättra felhanteringen för Test-AzDeployment och Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="09d17-427">Improve error handling for for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="09d17-428">Hantera fel utanför distributionsvalideringen och ta med dem i kommandoutdata istället</span><span class="sxs-lookup"><span data-stu-id="09d17-428">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="09d17-429">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="09d17-429">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="09d17-430">Lägg till växlingsparametern -IgnoreDynamicParameters till en uppsättning av cmdletar för distribution för att hoppa över fråga i skript och jobbscenarier</span><span class="sxs-lookup"><span data-stu-id="09d17-430">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="09d17-431">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="09d17-431">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="09d17-432">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="09d17-432">Az.Sql</span></span>
* <span data-ttu-id="09d17-433">Stöd för dataklassificering av databaser.</span><span class="sxs-lookup"><span data-stu-id="09d17-433">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="09d17-434">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="09d17-434">Az.Storage</span></span>
* <span data-ttu-id="09d17-435">Rapportera detaljfel när lagringskontext skapas med parametern -UseConnectedAccount, men utan inloggning på Azure-kontot</span><span class="sxs-lookup"><span data-stu-id="09d17-435">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="09d17-436">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="09d17-436">New-AzStorageContext</span></span>
* <span data-ttu-id="09d17-437">Stöd för att hantera Blob Service-egenskaper för ett angivet lagringskonto med API:et för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="09d17-437">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="09d17-438">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="09d17-438">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="09d17-439">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="09d17-439">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="09d17-440">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="09d17-440">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="09d17-441">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="09d17-441">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="09d17-442">Stöd för -AsJob-cmdletar för att ladda upp och ladda ned blobar och filer</span><span class="sxs-lookup"><span data-stu-id="09d17-442">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="09d17-443">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="09d17-443">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="09d17-444">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="09d17-444">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="09d17-445">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="09d17-445">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="09d17-446">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="09d17-446">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="09d17-447">1.6.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="09d17-447">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="09d17-448">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="09d17-448">Highlights since the last major release</span></span>
* <span data-ttu-id="09d17-449">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="09d17-449">General availability of `Az` module</span></span>
* <span data-ttu-id="09d17-450">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="09d17-450">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="09d17-451">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="09d17-451">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="09d17-452">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="09d17-452">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="09d17-453">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="09d17-453">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="09d17-454">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="09d17-454">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="09d17-455">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="09d17-455">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="09d17-456">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="09d17-456">Az.Automation</span></span>
* <span data-ttu-id="09d17-457">Azure Automation – ändring av uppdateringshantering för stöd för de nya funktionerna:</span><span class="sxs-lookup"><span data-stu-id="09d17-457">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="09d17-458">Dynamisk gruppering</span><span class="sxs-lookup"><span data-stu-id="09d17-458">Dynamic grouping</span></span>
    * <span data-ttu-id="09d17-459">För-/efterskrift</span><span class="sxs-lookup"><span data-stu-id="09d17-459">Pre-Post script</span></span>
    * <span data-ttu-id="09d17-460">Inställning för omstart</span><span class="sxs-lookup"><span data-stu-id="09d17-460">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="09d17-461">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="09d17-461">Az.Compute</span></span>
* <span data-ttu-id="09d17-462">Åtgärda problem med sökvägsmatchning i Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="09d17-462">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="09d17-463">Uppdatera Compute-klientbibliotek till 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="09d17-463">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="09d17-464">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="09d17-464">Az.KeyVault</span></span>
* <span data-ttu-id="09d17-465">Stöd för jokertecken för KeyVault-cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="09d17-465">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="09d17-466">Az.Network</span><span class="sxs-lookup"><span data-stu-id="09d17-466">Az.Network</span></span>
* <span data-ttu-id="09d17-467">Lägg till stöd för Threat Intelligence för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="09d17-467">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="09d17-468">Lägg till resurs för brandväggsprincip på översta nivå och anpassade regler för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="09d17-468">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="09d17-469">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="09d17-469">Az.RecoveryServices</span></span>
* <span data-ttu-id="09d17-470">SnapshotRetentionInDays har lagts till i Azure-principen för virtuella datorer för stöd av Instant RP</span><span class="sxs-lookup"><span data-stu-id="09d17-470">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="09d17-471">Pipe-stöd för avregistrering av container har lagts till</span><span class="sxs-lookup"><span data-stu-id="09d17-471">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="09d17-472">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="09d17-472">Az.Resources</span></span>
* <span data-ttu-id="09d17-473">Uppdatera stöd för jokertecken för Get-AzResource och Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="09d17-473">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="09d17-474">Uppdatera autentiseringsuppgifter som används vid allmänna anrop till ARM</span><span class="sxs-lookup"><span data-stu-id="09d17-474">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="09d17-475">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="09d17-475">Az.Sql</span></span>
* <span data-ttu-id="09d17-476">Cmdlet-parametern (ExcludeDetectionType) för Hotidentifiering ändrades från DetectionType till sträng[] för att framtidssäkra den när nya DetectionTypes läggs till, och även för att stödja automatisk ifyllning.</span><span class="sxs-lookup"><span data-stu-id="09d17-476">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="09d17-477">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="09d17-477">Az.Storage</span></span>
* <span data-ttu-id="09d17-478">Stöd för att hämta/ange/ta bort hanteringsprincip på ett lagringskonto</span><span class="sxs-lookup"><span data-stu-id="09d17-478">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="09d17-479">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="09d17-479">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="09d17-480">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="09d17-480">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="09d17-481">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="09d17-481">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="09d17-482">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="09d17-482">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="09d17-483">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="09d17-483">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="09d17-484">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="09d17-484">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="09d17-485">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="09d17-485">Az.Websites</span></span>
* <span data-ttu-id="09d17-486">Åtgärda fel med ARM-mall som avbryter kloning av alla platser med 'New-AzWebApp -IncludeSourceWebAppSlots'</span><span class="sxs-lookup"><span data-stu-id="09d17-486">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="09d17-487">1.5.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="09d17-487">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="09d17-488">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="09d17-488">Az.Accounts</span></span>
* <span data-ttu-id="09d17-489">Lägg till kommandot Register-AzModule för stöd för AutoRest-genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="09d17-489">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="09d17-490">Uppdatera exempel för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="09d17-490">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="09d17-491">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="09d17-491">Az.Automation</span></span>
* <span data-ttu-id="09d17-492">Problem med att hämta vissa månadsscheman i flera Azure Automation-cmdletar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="09d17-492">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="09d17-493">Åtgärda problem med att Get-AzAutomationDscNode bara returnerar de 20 översta noderna.</span><span class="sxs-lookup"><span data-stu-id="09d17-493">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="09d17-494">Nu returneras alla noder</span><span class="sxs-lookup"><span data-stu-id="09d17-494">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="09d17-495">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="09d17-495">Az.Cdn</span></span>
* <span data-ttu-id="09d17-496">Nya Powershell-cmdletar för att aktivera/inaktivera anpassade domän-HTTPS har lagts till och de gamla har gjorts inaktuella</span><span class="sxs-lookup"><span data-stu-id="09d17-496">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="09d17-497">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="09d17-497">Az.Compute</span></span>
* <span data-ttu-id="09d17-498">Lägg till stöd för jokertecken för Get-cmdletar</span><span class="sxs-lookup"><span data-stu-id="09d17-498">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="09d17-499">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="09d17-499">Az.DataFactory</span></span>
* <span data-ttu-id="09d17-500">ADF .Net SDK-versionen har uppdaterats till 3.0.1</span><span class="sxs-lookup"><span data-stu-id="09d17-500">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="09d17-501">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="09d17-501">Az.LogicApp</span></span>
* <span data-ttu-id="09d17-502">Åtgärda problemet med att ListWorkflows endast hämtar den första sidan med resultat</span><span class="sxs-lookup"><span data-stu-id="09d17-502">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="09d17-503">Az.Network</span><span class="sxs-lookup"><span data-stu-id="09d17-503">Az.Network</span></span>
* <span data-ttu-id="09d17-504">Lägg till stöd för jokertecken för Network-cmdletar</span><span class="sxs-lookup"><span data-stu-id="09d17-504">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="09d17-505">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="09d17-505">Az.RecoveryServices</span></span>
* <span data-ttu-id="09d17-506">Stöd har lagts till för SQL Server i virtuella Azure-datorer</span><span class="sxs-lookup"><span data-stu-id="09d17-506">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="09d17-507">SDK-uppdatering</span><span class="sxs-lookup"><span data-stu-id="09d17-507">SDK Update</span></span>
* <span data-ttu-id="09d17-508">Get-ProtectableItem-incheckning i VMappContainer har tagits bort</span><span class="sxs-lookup"><span data-stu-id="09d17-508">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="09d17-509">Name och ServerName har lagts till som parametrar för Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="09d17-509">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="09d17-510">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="09d17-510">Az.Resources</span></span>
* <span data-ttu-id="09d17-511">Lägg till parametern `-TemplateObject` i cmdletar för distribution</span><span class="sxs-lookup"><span data-stu-id="09d17-511">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="09d17-512">Mer information här: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="09d17-512">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="09d17-513">Åtgärda problem med piping av resultatet i `Get-AzResource` till `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="09d17-513">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="09d17-514">Mer information här: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="09d17-514">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="09d17-515">Åtgärda problem med ändring av JSON-datatyp när `Set-AzResource` körs</span><span class="sxs-lookup"><span data-stu-id="09d17-515">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="09d17-516">Mer information här: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="09d17-516">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="09d17-517">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="09d17-517">Az.Sql</span></span>
* <span data-ttu-id="09d17-518">AuditingEndpointsCommunicator uppdateras.</span><span class="sxs-lookup"><span data-stu-id="09d17-518">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="09d17-519">Åtgärdar beteendet hos ett gränsscenario när nya diagnostikinställningar skapas.</span><span class="sxs-lookup"><span data-stu-id="09d17-519">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="09d17-520">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="09d17-520">Az.Storage</span></span>
* <span data-ttu-id="09d17-521">Stöd för BlockBlobStorage när Storage-konto skapas      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="09d17-521">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="09d17-522">1.4.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="09d17-522">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="09d17-523">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="09d17-523">Az.AnalysisServices</span></span>
* <span data-ttu-id="09d17-524">Inaktuell AddAzureASAccount-cmdlet</span><span class="sxs-lookup"><span data-stu-id="09d17-524">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="09d17-525">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="09d17-525">Az.Automation</span></span>
* <span data-ttu-id="09d17-526">Hjälpen för Import-AzAutomationDscNodeConfiguration har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="09d17-526">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="09d17-527">Konfigurationsnamnsvalidering har lagts till i cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="09d17-527">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="09d17-528">Förbättrad felhantering för cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="09d17-528">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="09d17-529">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="09d17-529">Az.CognitiveServices</span></span>
* <span data-ttu-id="09d17-530">CustomSubdomainName har lagts till som en ny valfri parameter för New-AzCognitiveServicesAccount, som används för att ange underdomän för resursen.</span><span class="sxs-lookup"><span data-stu-id="09d17-530">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="09d17-531">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="09d17-531">Az.Compute</span></span>
* <span data-ttu-id="09d17-532">Problemet med ID-parameteruppsättningar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="09d17-532">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="09d17-533">Get-AzVMExtension har uppdaterats så att alla installerade tillägg visas om parametern Name inte har angetts</span><span class="sxs-lookup"><span data-stu-id="09d17-533">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="09d17-534">Parametrarna Tag och ResourceId har lagts till i cmdleten Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="09d17-534">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="09d17-535">Get-AzVmssVM utan instans-ID och med InstanceView kan visa virtuella VMSS-datorer med instansvyn.</span><span class="sxs-lookup"><span data-stu-id="09d17-535">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="09d17-536">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="09d17-536">Az.DataLakeStore</span></span>
* <span data-ttu-id="09d17-537">Cmdletar har lagts till för uppräkning och återställning av borttagna objekt i ADL</span><span class="sxs-lookup"><span data-stu-id="09d17-537">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="09d17-538">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="09d17-538">Az.EventHub</span></span>
* <span data-ttu-id="09d17-539">Ny boolesk egenskap SkipEmptyArchives har lagts till i Skip Empty Archives i CaptureDescription-klassen i Eventhub</span><span class="sxs-lookup"><span data-stu-id="09d17-539">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="09d17-540">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="09d17-540">Az.KeyVault</span></span>
* <span data-ttu-id="09d17-541">Taggning i Set-AzKeyVaultSecret har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="09d17-541">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="09d17-542">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="09d17-542">Az.LogicApp</span></span>
* <span data-ttu-id="09d17-543">Grundläggande SKU har lagts till för Integrationskonton</span><span class="sxs-lookup"><span data-stu-id="09d17-543">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="09d17-544">XSLT 2.0, XSLT 3.0 och Flytande mappningstyper har lagts till</span><span class="sxs-lookup"><span data-stu-id="09d17-544">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="09d17-545">Nya cmdletar för integrationskontosammansättningar</span><span class="sxs-lookup"><span data-stu-id="09d17-545">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="09d17-546">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="09d17-546">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="09d17-547">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="09d17-547">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="09d17-548">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="09d17-548">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="09d17-549">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="09d17-549">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="09d17-550">Nya cmdletar för batchkonfiguration för integrationskonto</span><span class="sxs-lookup"><span data-stu-id="09d17-550">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="09d17-551">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="09d17-551">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="09d17-552">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="09d17-552">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="09d17-553">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="09d17-553">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="09d17-554">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="09d17-554">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="09d17-555">Logic App-SDK har uppdaterats till version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="09d17-555">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="09d17-556">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="09d17-556">Az.Monitor</span></span>
* <span data-ttu-id="09d17-557">Hjälpen för Get-AzMetric har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="09d17-557">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="09d17-558">Az.Network</span><span class="sxs-lookup"><span data-stu-id="09d17-558">Az.Network</span></span>
* <span data-ttu-id="09d17-559">Hjälpexempel för Add-AzApplicationGatewayCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="09d17-559">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="09d17-560">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="09d17-560">Az.OperationalInsights</span></span>
* <span data-ttu-id="09d17-561">Ytterligare stöd för datakällorna New och Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="09d17-561">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="09d17-562">Ny ApplicationInsights-typ har lagts till för att ge stöd för ”Get specific” och ”Get all” för ApplicationInsights-datakällor för angiven arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="09d17-562">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="09d17-563">Cmdleten New-AzOperationalInsightsApplicationInsightsDataSource har lagts till för att skapa datakälla med angivna parametrar för Application Insights-resurs: subscription Id, resourceGroupName och name.</span><span class="sxs-lookup"><span data-stu-id="09d17-563">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="09d17-564">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="09d17-564">Az.Resources</span></span>
* <span data-ttu-id="09d17-565">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="09d17-565">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="09d17-566">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="09d17-566">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="09d17-567">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="09d17-567">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="09d17-568">Fel som gör att KeyCredentials inte kan skapas upprepade gånger har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="09d17-568">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="09d17-569">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="09d17-569">Az.Sql</span></span>
* <span data-ttu-id="09d17-570">Lägg till stöd för hyperskalanivån för SQL DB</span><span class="sxs-lookup"><span data-stu-id="09d17-570">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="09d17-571">Ett fel har åtgärdats där återställningen kunde misslyckas på grund av onödiga inställningsegenskaper i restore-förfrågan</span><span class="sxs-lookup"><span data-stu-id="09d17-571">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="09d17-572">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="09d17-572">Az.Websites</span></span>
* <span data-ttu-id="09d17-573">Rätt exempel i Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="09d17-573">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="09d17-574">1.3.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="09d17-574">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="09d17-575">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="09d17-575">Az.Accounts</span></span>
* <span data-ttu-id="09d17-576">Uppdatera till den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="09d17-576">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="09d17-577">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="09d17-577">Az.AnalysisServices</span></span>
<span data-ttu-id="09d17-578">Allmän tillgänglighet för Az.AnalysisServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="09d17-578">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="09d17-579">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="09d17-579">Az.Compute</span></span>
* <span data-ttu-id="09d17-580">AEM-tillägg: Lägg till stöd för UltraSSD-, P60-, P70- och P80-diskar</span><span class="sxs-lookup"><span data-stu-id="09d17-580">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="09d17-581">Uppdatera hjälpbeskrivning för Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="09d17-581">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="09d17-582">Uppdatera hjälpbeskrivning och exempel för Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="09d17-582">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="09d17-583">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="09d17-583">Az.RecoveryServices</span></span>
<span data-ttu-id="09d17-584">Allmän tillgänglighet för Az.RecoveryServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="09d17-584">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="09d17-585">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="09d17-585">Az.Resources</span></span>
* <span data-ttu-id="09d17-586">Korrigera taggar för resursgrupper</span><span class="sxs-lookup"><span data-stu-id="09d17-586">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="09d17-587">Mer information här: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="09d17-587">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="09d17-588">Åtgärda problem där `Get-AzureRmRoleAssignment` inte respekterar -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="09d17-588">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="09d17-589">Mer information här: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="09d17-589">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="09d17-590">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="09d17-590">Az.Sql</span></span>
* <span data-ttu-id="09d17-591">Lägga till Get/Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="09d17-591">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="09d17-592">Åtgärda problem där ett nullref-undantag uppstår när du kör SQL-cmdletar och inte är inloggad på ett Azure-konto</span><span class="sxs-lookup"><span data-stu-id="09d17-592">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="09d17-593">Åtgärda nullref-undantag i Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="09d17-593">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="09d17-594">1.2.1 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="09d17-594">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="09d17-595">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="09d17-595">Az.Accounts</span></span>
* <span data-ttu-id="09d17-596">Version med rätt version av autentisering</span><span class="sxs-lookup"><span data-stu-id="09d17-596">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="09d17-597">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="09d17-597">Az.AnalysisServices</span></span>
* <span data-ttu-id="09d17-598">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="09d17-598">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="09d17-599">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="09d17-599">Az.RecoveryServices</span></span>
* <span data-ttu-id="09d17-600">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="09d17-600">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="09d17-601">1.2.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="09d17-601">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="09d17-602">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="09d17-602">Az.Accounts</span></span>
* <span data-ttu-id="09d17-603">Lägga till interaktiv autentisering och autentisering med användarnamn/lösenord för endast Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="09d17-603">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="09d17-604">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="09d17-604">Update incorrect online help URLs</span></span>
* <span data-ttu-id="09d17-605">Lägga till varningsmeddelande i PS Core för Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="09d17-605">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="09d17-606">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="09d17-606">Az.Aks</span></span>
* <span data-ttu-id="09d17-607">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="09d17-607">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="09d17-608">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="09d17-608">Az.Automation</span></span>
* <span data-ttu-id="09d17-609">Stöd för Python 2-runbookflöden har lagts till</span><span class="sxs-lookup"><span data-stu-id="09d17-609">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="09d17-610">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="09d17-610">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="09d17-611">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="09d17-611">Az.Cdn</span></span>
* <span data-ttu-id="09d17-612">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="09d17-612">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="09d17-613">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="09d17-613">Az.Compute</span></span>
* <span data-ttu-id="09d17-614">Lägga till cmdleten Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="09d17-614">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="09d17-615">Lägga till TempDisk-parameter i Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="09d17-615">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="09d17-616">Korrigera varningsmeddelande för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="09d17-616">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="09d17-617">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="09d17-617">Az.ContainerRegistry</span></span>
* <span data-ttu-id="09d17-618">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="09d17-618">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="09d17-619">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="09d17-619">Az.DataFactory</span></span>
* <span data-ttu-id="09d17-620">ADF .Net SDK-versionen har uppdaterats till 3.0.0</span><span class="sxs-lookup"><span data-stu-id="09d17-620">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="09d17-621">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="09d17-621">Az.DataLakeStore</span></span>
* <span data-ttu-id="09d17-622">Åtgärda problem med ADLS-slutpunkt vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="09d17-622">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="09d17-623">Mer information här: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="09d17-623">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="09d17-624">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="09d17-624">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="09d17-625">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="09d17-625">Az.IotHub</span></span>
* <span data-ttu-id="09d17-626">Lägga till kodningsformat i cmdleten Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="09d17-626">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="09d17-627">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="09d17-627">Az.KeyVault</span></span>
* <span data-ttu-id="09d17-628">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="09d17-628">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="09d17-629">Az.Network</span><span class="sxs-lookup"><span data-stu-id="09d17-629">Az.Network</span></span>
* <span data-ttu-id="09d17-630">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="09d17-630">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="09d17-631">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="09d17-631">Az.Resources</span></span>
* <span data-ttu-id="09d17-632">Åtgärda felaktiga exempel i referensdokumentationen ”New-AzADAppCredential” och ”New-AzADSpCredential”</span><span class="sxs-lookup"><span data-stu-id="09d17-632">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="09d17-633">Åtgärda problem där sökvägen för parametern ”-TemplateFile” inte omvandlas innan cmdletarna för distribution i resursgruppen körs</span><span class="sxs-lookup"><span data-stu-id="09d17-633">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="09d17-634">Az.Resources: Korrigera dokumentationen om standardvärdet för New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="09d17-634">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="09d17-635">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="09d17-635">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="09d17-636">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="09d17-636">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="09d17-637">Åtgärda formateringsproblemet med objektet ”PSResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="09d17-637">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="09d17-638">Mer information här: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="09d17-638">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="09d17-639">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="09d17-639">Az.ServiceFabric</span></span>
* <span data-ttu-id="09d17-640">Återställ när ett certifikat läggs till i en Virtual Machine Scale Sets-modell men ett undantag genereras. Detta har gjorts för att åtgärda följande fel: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="09d17-640">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="09d17-641">Korrigera några felmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="09d17-641">Fix some error messages.</span></span>
* <span data-ttu-id="09d17-642">Korrigering av skapande av kluster med ARM-mall som är standard för New-AzServiceFabriCluster som inte fungerade med migrering till Az.</span><span class="sxs-lookup"><span data-stu-id="09d17-642">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="09d17-643">Korrigering av tilläggning av kluster/programcertifikat så att endast VM Scale Sets som motsvarar klustret läggs till genom att kontrollera ID för klustret i tillägget.</span><span class="sxs-lookup"><span data-stu-id="09d17-643">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="09d17-644">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="09d17-644">Az.SignalR</span></span>
* <span data-ttu-id="09d17-645">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="09d17-645">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="09d17-646">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="09d17-646">Az.Sql</span></span>
* <span data-ttu-id="09d17-647">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="09d17-647">Update incorrect online help URLs</span></span>
* <span data-ttu-id="09d17-648">Uppdaterad parameterbeskrivning för LicenseType-parameter med möjliga värden</span><span class="sxs-lookup"><span data-stu-id="09d17-648">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="09d17-649">Korrigering för att uppdatera hanterad instansidentitet som inte fungerar när det är den enda uppdaterade egenskapen</span><span class="sxs-lookup"><span data-stu-id="09d17-649">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="09d17-650">Stöd för anpassad sortering på hanterad instans</span><span class="sxs-lookup"><span data-stu-id="09d17-650">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="09d17-651">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="09d17-651">Az.Storage</span></span>
* <span data-ttu-id="09d17-652">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="09d17-652">Update incorrect online help URLs</span></span>
* <span data-ttu-id="09d17-653">Tillhandahåll detaljerat felmeddelande när en användare försöker hämta/konfigurera klassisk loggning/mått på ett Premium Storage-konto eftersom Premium Storage-kontot inte har stöd för klassisk loggning/mått.</span><span class="sxs-lookup"><span data-stu-id="09d17-653">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="09d17-654">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="09d17-654">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="09d17-655">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="09d17-655">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="09d17-656">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="09d17-656">Az.TrafficManager</span></span>
* <span data-ttu-id="09d17-657">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="09d17-657">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="09d17-658">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="09d17-658">Az.Websites</span></span>
* <span data-ttu-id="09d17-659">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="09d17-659">Update incorrect online help URLs</span></span>
* <span data-ttu-id="09d17-660">Korrigerar ”New-AzWebAppSSLBinding” så att certifikatet laddas upp till rätt resursgrupp och plats om appen finns i en ASE.</span><span class="sxs-lookup"><span data-stu-id="09d17-660">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="09d17-661">Korrigerar ”New-AzWebAppSSLBinding” så att taggarna inte skrivs över på en bindning av ett SSL-certifikat till en app</span><span class="sxs-lookup"><span data-stu-id="09d17-661">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="09d17-662">1.1.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="09d17-662">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="09d17-663">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="09d17-663">Az.Accounts</span></span>
* <span data-ttu-id="09d17-664">Lade till omfattningen ”Lokal” till Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="09d17-664">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="09d17-665">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="09d17-665">Az.Compute</span></span>
* <span data-ttu-id="09d17-666">Namn är nu valfritt i ID-parametern för Restart/Start/Stop/Remove/Set-AzVM och Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="09d17-666">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="09d17-667">Uppdaterade beskrivningen av ID i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="09d17-667">Updated the description of ID in help files</span></span>
* <span data-ttu-id="09d17-668">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="09d17-668">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="09d17-669">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="09d17-669">Az.DataLakeStore</span></span>
* <span data-ttu-id="09d17-670">Uppdatera sdk-versionen av dataplanet till 1.1.14 för SDK-korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="09d17-670">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="09d17-671">Korrigerade hanteringen av negativ accesstime och modificationtime för getfilestatus och liststatus; korrigera asynkront annulleringstoken</span><span class="sxs-lookup"><span data-stu-id="09d17-671">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="09d17-672">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="09d17-672">Az.EventGrid</span></span>
* <span data-ttu-id="09d17-673">Uppdaterat för användning av API-versionen 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="09d17-673">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="09d17-674">Uppdaterade följande cmdletar för att stödja nytt scenario i API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="09d17-674">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="09d17-675">New-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="09d17-675">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="09d17-676">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="09d17-676">Event Time-To-Live,</span></span>
        - <span data-ttu-id="09d17-677">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="09d17-677">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="09d17-678">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="09d17-678">Dead letter endpoint.</span></span>
    - <span data-ttu-id="09d17-679">Update-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="09d17-679">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="09d17-680">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="09d17-680">Event Time-To-Live,</span></span>
        - <span data-ttu-id="09d17-681">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="09d17-681">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="09d17-682">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="09d17-682">Dead letter endpoint.</span></span>
* <span data-ttu-id="09d17-683">Lade till nya enum-värden (storageQueue och hybridConnection) för alternativet EndpointType i cmdletarna New-AzureRmEventGridSubscription och Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="09d17-683">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="09d17-684">Visa varningsmeddelanden om skapande eller uppdatering av händelseprenumerationen förväntas medföra manuell åtgärd från användaren.</span><span class="sxs-lookup"><span data-stu-id="09d17-684">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="09d17-685">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="09d17-685">Az.IotHub</span></span>
* <span data-ttu-id="09d17-686">Har uppdaterats till den senaste versionen av SDK:n lotHub</span><span class="sxs-lookup"><span data-stu-id="09d17-686">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="09d17-687">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="09d17-687">Az.LogicApp</span></span>
* <span data-ttu-id="09d17-688">Get-AzLogicApp visar en lista över alla som inte har angivet namn</span><span class="sxs-lookup"><span data-stu-id="09d17-688">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="09d17-689">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="09d17-689">Az.Resources</span></span>
* <span data-ttu-id="09d17-690">Åtgärdade problem med parameteruppsättningen när parametrarna -ODataQuery och -ResourceId anges för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="09d17-690">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="09d17-691">Mer information här: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="09d17-691">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="09d17-692">Åtgärdade hantering av parametern -Custom i New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="09d17-692">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="09d17-693">Korrigerade stavfel i New-AzDeployment-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="09d17-693">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="09d17-694">Gjorde parametern -MailNickname obligatorisk för New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="09d17-694">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="09d17-695">Mer information här: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="09d17-695">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="09d17-696">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="09d17-696">Az.SignalR</span></span>
* <span data-ttu-id="09d17-697">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="09d17-697">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="09d17-698">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="09d17-698">Az.Sql</span></span>
* <span data-ttu-id="09d17-699">Konverterade lagringshanteringsklientens beroende av den normala SDK-implementeringen.</span><span class="sxs-lookup"><span data-stu-id="09d17-699">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="09d17-700">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="09d17-700">Az.Storage</span></span>
* <span data-ttu-id="09d17-701">Angav StorageAccountName för lagringskontext som det verkliga namnet på lagringskontot när det skapas med Sas Token, OAuth eller Anonymous</span><span class="sxs-lookup"><span data-stu-id="09d17-701">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="09d17-702">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="09d17-702">New-AzStorageContext</span></span>
* <span data-ttu-id="09d17-703">Skapade Sas Token för Blob Snapshot-objekt med parametern -FullUri, åtgärdade den returnerade URI:n så att den blir URI för ögonblicksbild</span><span class="sxs-lookup"><span data-stu-id="09d17-703">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="09d17-704">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="09d17-704">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="09d17-705">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="09d17-705">Az.Websites</span></span>
* <span data-ttu-id="09d17-706">Åtgärdade en bugg i datumparsningen i Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="09d17-706">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="09d17-707">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="09d17-707">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="09d17-708">1.0.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="09d17-708">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="09d17-709">Allmänt</span><span class="sxs-lookup"><span data-stu-id="09d17-709">General</span></span>

- <span data-ttu-id="09d17-710">Allmän tillgänglighet för Az-modulen</span><span class="sxs-lookup"><span data-stu-id="09d17-710">General Availability of Az Module</span></span>
- <span data-ttu-id="09d17-711">Onlinehjälp för varje modul</span><span class="sxs-lookup"><span data-stu-id="09d17-711">Online help for each module</span></span>
- <span data-ttu-id="09d17-712">Mer information och en översikt finns på [Az-informationssidan](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="09d17-712">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="09d17-713">Information om hur du migrerar från AzureRM finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="09d17-713">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="09d17-714">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="09d17-714">Az.Accounts</span></span>
- <span data-ttu-id="09d17-715">Har ändrats från Az.Profile</span><span class="sxs-lookup"><span data-stu-id="09d17-715">Changed from Az.Profile</span></span>
- <span data-ttu-id="09d17-716">Fasta tabellformat för profil- och kontexttyper</span><span class="sxs-lookup"><span data-stu-id="09d17-716">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="09d17-717">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="09d17-717">Az.ApiManagement</span></span>
- <span data-ttu-id="09d17-718">Korrigeringar för #7002</span><span class="sxs-lookup"><span data-stu-id="09d17-718">Fixes for #7002</span></span>
- <span data-ttu-id="09d17-719">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="09d17-719">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="09d17-720">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="09d17-720">Az.Batch</span></span>
- <span data-ttu-id="09d17-721">Lade till möjligheten att se vilken version av Azure Batch Node Agent som körs på var och en av de virtuella datorerna i en pool, via den nya egenskapen `NodeAgentInformation` på `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="09d17-721">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="09d17-722">Standarden `Caching` för `PSDataDisk` är nu `ReadWrite` i stället för `None`.</span><span class="sxs-lookup"><span data-stu-id="09d17-722">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="09d17-723">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="09d17-723">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="09d17-724">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="09d17-724">Az.Billing</span></span>
- <span data-ttu-id="09d17-725">Kombinerar cmdletarna för fakturering, förbrukning och UsageAggregates. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="09d17-725">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="09d17-726">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="09d17-726">Az.CognitivServices</span></span>
- <span data-ttu-id="09d17-727">Lade till kompletterare för SkuName och Typem som är tillgängliga i New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="09d17-727">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="09d17-728">Tog bort parameteruppsättningen GetSkusWithAccountParamSetName från Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="09d17-728">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="09d17-729">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="09d17-729">Az.ContainerInstance</span></span>
- <span data-ttu-id="09d17-730">Stöd för ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="09d17-730">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="09d17-731">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="09d17-731">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="09d17-732">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="09d17-732">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="09d17-733">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="09d17-733">Az.DataLakeStore</span></span>
- <span data-ttu-id="09d17-734">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="09d17-734">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="09d17-735">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="09d17-735">Az.Monitor</span></span>
- <span data-ttu-id="09d17-736">Döpte om Az.Insights till Az.Monitor och andra mindre icke-bakåtkompatibla ändringar. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="09d17-736">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="09d17-737">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="09d17-737">Az.KeyVault</span></span>
- <span data-ttu-id="09d17-738">Tog bort den inaktuella egenskapen PurgeDisabled från utdatatyper</span><span class="sxs-lookup"><span data-stu-id="09d17-738">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="09d17-739">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="09d17-739">Az.MachineLearning</span></span>
- <span data-ttu-id="09d17-740">Inkluderade cmdletarna från modulen Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="09d17-740">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="09d17-741">Az.Media</span><span class="sxs-lookup"><span data-stu-id="09d17-741">Az.Media</span></span>
- <span data-ttu-id="09d17-742">Tog bort inaktuella -Tags-alias från New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="09d17-742">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="09d17-743">Az.Network</span><span class="sxs-lookup"><span data-stu-id="09d17-743">Az.Network</span></span>
<span data-ttu-id="09d17-744">Stöd har lagts till för konfiguration av RewriteRuleSets i Application Gateway</span><span class="sxs-lookup"><span data-stu-id="09d17-744">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="09d17-745">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="09d17-745">New cmdlets added:</span></span>
        - <span data-ttu-id="09d17-746">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="09d17-746">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="09d17-747">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="09d17-747">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="09d17-748">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="09d17-748">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="09d17-749">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="09d17-749">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="09d17-750">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="09d17-750">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="09d17-751">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="09d17-751">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="09d17-752">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="09d17-752">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="09d17-753">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="09d17-753">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="09d17-754">Cmdletar har uppdaterats med den valfria parametern -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="09d17-754">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="09d17-755">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="09d17-755">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="09d17-756">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="09d17-756">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="09d17-757">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="09d17-757">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="09d17-758">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="09d17-758">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="09d17-759">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="09d17-759">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="09d17-760">New-AzureRmApplicationGatewayUrlPathMapConfig har lagt till KeyVault-stöd för Application Gateway med Identity.</span><span class="sxs-lookup"><span data-stu-id="09d17-760">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="09d17-761">Cmdletar har uppdaterats med den valfria parametern -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="09d17-761">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="09d17-762">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="09d17-762">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="09d17-763">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="09d17-763">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="09d17-764">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="09d17-764">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="09d17-765">Cmdleten New-AzApplicationGateway har uppdaterats med den valfria parametern -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="09d17-765">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="09d17-766">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="09d17-766">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="09d17-767">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="09d17-767">Az.OperationalInsights</span></span>
- <span data-ttu-id="09d17-768">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="09d17-768">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="09d17-769">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="09d17-769">Az.Profile</span></span>
- <span data-ttu-id="09d17-770">Modulnamnet har ändrats till Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="09d17-770">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="09d17-771">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="09d17-771">Az.RecoveryServices</span></span>
- <span data-ttu-id="09d17-772">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="09d17-772">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="09d17-773">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="09d17-773">Az.Resources</span></span>
- <span data-ttu-id="09d17-774">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="09d17-774">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="09d17-775">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="09d17-775">Az.ServiceFabric</span></span>
- <span data-ttu-id="09d17-776">Stöd för specificering av certifikat efter eget namn och tumavtryck</span><span class="sxs-lookup"><span data-stu-id="09d17-776">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="09d17-777">Information om fler icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="09d17-777">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="09d17-778">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="09d17-778">Az.SIgnalR</span></span>
- <span data-ttu-id="09d17-779">Allmän tillgänglighet för PowerShell-cmdletar för SIgnalR</span><span class="sxs-lookup"><span data-stu-id="09d17-779">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="09d17-780">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="09d17-780">Az.Sql</span></span>
- <span data-ttu-id="09d17-781">Lade till de nya identifieringstyperna Data_Exfiltration och Unsafe_Action i Threat Detection-cmdletar</span><span class="sxs-lookup"><span data-stu-id="09d17-781">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="09d17-782">Uppdaterade dokumentationsexempel för Sql Auditing-cmdletar</span><span class="sxs-lookup"><span data-stu-id="09d17-782">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="09d17-783">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="09d17-783">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="09d17-784">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="09d17-784">Az.Storage</span></span>
- <span data-ttu-id="09d17-785">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="09d17-785">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="09d17-786">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="09d17-786">Az.Websites</span></span>
- <span data-ttu-id="09d17-787">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="09d17-787">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="09d17-788">0.7.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="09d17-788">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="09d17-789">Allmänt</span><span class="sxs-lookup"><span data-stu-id="09d17-789">General</span></span>

* <span data-ttu-id="09d17-790">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="09d17-790">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="09d17-791">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="09d17-791">Az.Compute</span></span>

* <span data-ttu-id="09d17-792">Lade till stöd för UltraSSD och Galleriavbildningar i de enkla parameteruppsättningarna för `New-AzVm(ss)`-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="09d17-792">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="09d17-793">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="09d17-793">Az.DataLakeStore</span></span>

* <span data-ttu-id="09d17-794">Åtgärdade avslutande snedstreck i domänen för adls-konto</span><span class="sxs-lookup"><span data-stu-id="09d17-794">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="09d17-795">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="09d17-795">Az.FrontDoor</span></span>

* <span data-ttu-id="09d17-796">Brutna länkar korrigerades</span><span class="sxs-lookup"><span data-stu-id="09d17-796">Fixed some broken links</span></span>
    - <span data-ttu-id="09d17-797">I artiklarna New-AzureRmFrontDoor och Set-AzureRmFrontDoor artiklar korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="09d17-797">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="09d17-798">I artikeln New-AzureRmFrontDoorManagedRuleObject korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="09d17-798">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="09d17-799">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="09d17-799">Az.RecoveryServices</span></span>

* <span data-ttu-id="09d17-800">Lade till valideringar på klientsidan för Azure-filresurs med återställningsåtgärder.</span><span class="sxs-lookup"><span data-stu-id="09d17-800">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="09d17-801">Gjorde storageAccountName och storageAccountResourceGroupName valfritt för afs-återställning.</span><span class="sxs-lookup"><span data-stu-id="09d17-801">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="09d17-802">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="09d17-802">Az.Resources</span></span>

* <span data-ttu-id="09d17-803">Korrigering för https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="09d17-803">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="09d17-804">Uppdaterade Get-AzureRmRoleAssignment så att prenumerationsomfattningen används om den anges vid begäran om klassiska administratörer.</span><span class="sxs-lookup"><span data-stu-id="09d17-804">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="09d17-805">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="09d17-805">Az.Sql</span></span>

* <span data-ttu-id="09d17-806">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="09d17-806">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="09d17-807">Korrigerade ett problem med Get-AzureRmSqlDatabaseVulnerabilityAssessment med DotNet-kärna</span><span class="sxs-lookup"><span data-stu-id="09d17-807">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="09d17-808">Ändrade dokumentationen för hjälpmeddelanden som rör SQL Auditing-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="09d17-808">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="09d17-809">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="09d17-809">Az.Storage</span></span>

* <span data-ttu-id="09d17-810">Lade till -EnableHierarchicalNamespace i New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="09d17-810">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="09d17-811">Åtgärdade problemet med att cmdleten Copy File inte kunde återanvända källkontexten på målet om inte -DestContext angetts</span><span class="sxs-lookup"><span data-stu-id="09d17-811">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="09d17-812">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="09d17-812">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="09d17-813">Stöd för statisk webbplatskonfiguration</span><span class="sxs-lookup"><span data-stu-id="09d17-813">Support Static Website configuration</span></span>
    - <span data-ttu-id="09d17-814">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="09d17-814">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="09d17-815">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="09d17-815">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="09d17-816">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="09d17-816">Az.Websites</span></span>

* <span data-ttu-id="09d17-817">Set-AzureRmWebApp och Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="09d17-817">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="09d17-818">Ny parameter (-AzureStoragePath) har lagts till för att ange att Azure Storage-sökvägar ska monteras i containerappar i Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="09d17-818">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="09d17-819">Använder utdata från den nya cmdleten New-AzureRmWebAppAzureStoragePath som en parameter för att ange sökvägar för Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="09d17-819">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="09d17-820">0.6.1 – november 2018</span><span class="sxs-lookup"><span data-stu-id="09d17-820">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="09d17-821">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="09d17-821">Az.ApiManagement</span></span>
* <span data-ttu-id="09d17-822">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="09d17-822">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="09d17-823">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="09d17-823">Az.Automation</span></span>
* <span data-ttu-id="09d17-824">Swagger baserade Azure Automation-cmdletar</span><span class="sxs-lookup"><span data-stu-id="09d17-824">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="09d17-825">Cmdletar för Uppdateringshantering har lagts till</span><span class="sxs-lookup"><span data-stu-id="09d17-825">Added Update Management cmdlets</span></span>
* <span data-ttu-id="09d17-826">Cmdletar för källkontroll har lagts till</span><span class="sxs-lookup"><span data-stu-id="09d17-826">Added Source Control cmdlets</span></span>
* <span data-ttu-id="09d17-827">Remove-AzureRmAutomationHybridWorkerGroup-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="09d17-827">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="09d17-828">Kommandot för DSC-registreringsnod har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="09d17-828">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="09d17-829">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="09d17-829">Az.Compute</span></span>
* <span data-ttu-id="09d17-830">Problem med SystemAssigned-identitet har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="09d17-830">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="09d17-831">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="09d17-831">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="09d17-832">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="09d17-832">Az.ContainerInstance</span></span>
* <span data-ttu-id="09d17-833">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="09d17-833">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="09d17-834">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="09d17-834">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="09d17-835">uppdatera exempelbeskrivningen för marketplace-cmdletar</span><span class="sxs-lookup"><span data-stu-id="09d17-835">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="09d17-836">Az.Network</span><span class="sxs-lookup"><span data-stu-id="09d17-836">Az.Network</span></span>
* <span data-ttu-id="09d17-837">Cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomErreller Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="09d17-837">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="09d17-838">ICMP tillbaka till stöd för Azure Firewall-nätverksprotokoll har lagts till</span><span class="sxs-lookup"><span data-stu-id="09d17-838">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="09d17-839">Uppdatera cmdlet Test-AzureRmNetworkWatcherConnectivity, lägga till verifiering av mål-id, adress och port.</span><span class="sxs-lookup"><span data-stu-id="09d17-839">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="09d17-840">Åtgärda problem med minnesanvändning i VirtualNetwork-karta</span><span class="sxs-lookup"><span data-stu-id="09d17-840">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="09d17-841">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="09d17-841">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="09d17-842">Åtgärda för att ändra principen för en skyddad fildelning.</span><span class="sxs-lookup"><span data-stu-id="09d17-842">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="09d17-843">Tidszonsprincipen har konverterats till versaler.</span><span class="sxs-lookup"><span data-stu-id="09d17-843">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="09d17-844">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="09d17-844">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="09d17-845">Exempel i New-AzureRmRecoveryServicesAsrProtectableItem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="09d17-845">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="09d17-846">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="09d17-846">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="09d17-847">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="09d17-847">Az.Relay</span></span>
* <span data-ttu-id="09d17-848">Valfri parameter -KeyValue till New-AzureRmRelayKey cmdlet har lagts till, vilket gör det möjligt för användare att tillhandahålla KeyValue.</span><span class="sxs-lookup"><span data-stu-id="09d17-848">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="09d17-849">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="09d17-849">Az.Resources</span></span>
* <span data-ttu-id="09d17-850">Uppdatera hjälpdokumentation för resursidentitet kopplad till parametrar i `New-AzureRmPolicyAssignment` och `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="09d17-850">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="09d17-851">Lägg till ett exempel för New-AzureRmPolicyDefinition som använder -Metadata</span><span class="sxs-lookup"><span data-stu-id="09d17-851">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="09d17-852">Korrigera så att skiftläge behålls i taggnycklar i NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="09d17-852">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="09d17-853">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="09d17-853">Az.ServiceFabric</span></span>
* <span data-ttu-id="09d17-854">Lägg till utfasningsmeddelanden för kommande icke-kompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="09d17-854">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="09d17-855">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="09d17-855">Az.Sql</span></span>
* <span data-ttu-id="09d17-856">Nya cmdletar för CRUD-åtgärder på Azure Sql Database-hanterad instans och Azure Sql-hanterad databas</span><span class="sxs-lookup"><span data-stu-id="09d17-856">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="09d17-857">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="09d17-857">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="09d17-858">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="09d17-858">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="09d17-859">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="09d17-859">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="09d17-860">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="09d17-860">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="09d17-861">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="09d17-861">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="09d17-862">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="09d17-862">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="09d17-863">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="09d17-863">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="09d17-864">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="09d17-864">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="09d17-865">Hantering av utökad granskningsprincip på en server eller en databas har aktiverats.</span><span class="sxs-lookup"><span data-stu-id="09d17-865">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="09d17-866">Ny parameter (PredicateExpression) har lagts till för att aktivera filtrering av granskningsloggar.</span><span class="sxs-lookup"><span data-stu-id="09d17-866">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="09d17-867">Cmdletar har ändrats så att de använder SQL-klienter i stället för äldre klienter.</span><span class="sxs-lookup"><span data-stu-id="09d17-867">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="09d17-868">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="09d17-868">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="09d17-869">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="09d17-869">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="09d17-870">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="09d17-870">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="09d17-871">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="09d17-871">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="09d17-872">Problem med att använda Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings med lagringskontots namnparameter har korrigerats</span><span class="sxs-lookup"><span data-stu-id="09d17-872">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="09d17-873">0.5.0 – november 2018</span><span class="sxs-lookup"><span data-stu-id="09d17-873">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="09d17-874">Allmänt</span><span class="sxs-lookup"><span data-stu-id="09d17-874">General</span></span>
* <span data-ttu-id="09d17-875">Lade till resurskompletterare till många kärn-cmdletar – dessa gör att du kan stega genom befintliga resursnamn med TABB vid interaktiva anrop till cmdletar</span><span class="sxs-lookup"><span data-stu-id="09d17-875">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="09d17-876">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="09d17-876">Az.Profile</span></span>
* <span data-ttu-id="09d17-877">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="09d17-877">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="09d17-878">Bytte namn på parametern TenantId i cmdleten Connect-AzAccount till Tenant och lade till ett alias för TenantId</span><span class="sxs-lookup"><span data-stu-id="09d17-878">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="09d17-879">Uppdaterade TenantId-beskrivningen för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="09d17-879">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="09d17-880">Åtgärda felmeddelande för misslyckad inloggning när du tillhandahåller klientdomän</span><span class="sxs-lookup"><span data-stu-id="09d17-880">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="09d17-881">Åtgärda problem med att kontextnamn hamnar i konflikt för konton utan prenumerationer i klientorganisationen</span><span class="sxs-lookup"><span data-stu-id="09d17-881">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="09d17-882">Åtgärda problem med DataLake-slutpunkter vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="09d17-882">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="09d17-883">Åtgärdade problem med att Disconnect-AzAccount kastades om den inte anslöts</span><span class="sxs-lookup"><span data-stu-id="09d17-883">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="09d17-884">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="09d17-884">Az.CognitiveServices</span></span>
* <span data-ttu-id="09d17-885">Lade till åtgärden Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="09d17-885">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="09d17-886">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="09d17-886">Az.Compute</span></span>
* <span data-ttu-id="09d17-887">Lade till cmdletarna Add-AzVmssVMDataDisk och Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="09d17-887">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="09d17-888">Get-AzVMImage visar AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="09d17-888">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="09d17-889">Åtgärdade att värdena för alternativen SetAzVMChefExtension -BootstrapOptions och -JsonAttribute inte angavs i json-format.</span><span class="sxs-lookup"><span data-stu-id="09d17-889">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="09d17-890">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="09d17-890">Az.DataLakeStore</span></span>
* <span data-ttu-id="09d17-891">Uppdatera DataLake-paketet till 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="09d17-891">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="09d17-892">Lägg till standardsamtidighet för flertrådade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="09d17-892">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="09d17-893">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="09d17-893">Az.Insights</span></span>
* <span data-ttu-id="09d17-894">Åtgärdade problem #7267 (autoskalningsområde)</span><span class="sxs-lookup"><span data-stu-id="09d17-894">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="09d17-895">Problem med att uppräknade parametrar inte ställdes in ordentligt när du skapade en ny autoskalningsregel (de ställdes alltid in med standardvärdet).</span><span class="sxs-lookup"><span data-stu-id="09d17-895">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="09d17-896">Åtgärdade problem #7513 [Insights] Set-AzDiagnosticSetting kräver uttrycklig specifikation av kategorier när inställningar skapas</span><span class="sxs-lookup"><span data-stu-id="09d17-896">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="09d17-897">Nu kräver inte cmdleten uttrycklig anvisning av kategorierna för att aktiveras under skapande, d.v.s. den fungerar enligt beskrivning</span><span class="sxs-lookup"><span data-stu-id="09d17-897">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="09d17-898">Az.Network</span><span class="sxs-lookup"><span data-stu-id="09d17-898">Az.Network</span></span>
* <span data-ttu-id="09d17-899">PeeringType ändrades till en obligatorisk parameter för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="09d17-899">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="09d17-900">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="09d17-900">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="09d17-901">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="09d17-901">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="09d17-902">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="09d17-902">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="09d17-903">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="09d17-903">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="09d17-904">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="09d17-904">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="09d17-905">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="09d17-905">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="09d17-906">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="09d17-906">Az.PolicyInsights</span></span>
* <span data-ttu-id="09d17-907">Cmdletar för principreparation har lagts till</span><span class="sxs-lookup"><span data-stu-id="09d17-907">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="09d17-908">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="09d17-908">Az.Resources</span></span>
* <span data-ttu-id="09d17-909">Korrigering för https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="09d17-909">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="09d17-910">Tillåt att resurser listas med parametern -ResourceId för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="09d17-910">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="09d17-911">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="09d17-911">Az.ServiceBus</span></span>
* <span data-ttu-id="09d17-912">Skrivskyddad MigrationState-egenskap har lagts till i PSServiceBusMigrationConfigurationAttributes, som hjälper till att hålla koll på migreringstillståndet.</span><span class="sxs-lookup"><span data-stu-id="09d17-912">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="09d17-913">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="09d17-913">Az.ServiceFabric</span></span>
* <span data-ttu-id="09d17-914">Åtgärda att lägga till certifikat till Linux-Vmss.</span><span class="sxs-lookup"><span data-stu-id="09d17-914">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="09d17-915">Åtgärdade Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="09d17-915">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="09d17-916">Använd rätt tumavtryck från nya certifikat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="09d17-916">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="09d17-917">Visa undantag korrekt (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="09d17-917">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="09d17-918">Åtgärdade Update-AzServiceFabricDurability så att klusterkonfigurationen uppdateras innan Vmss-åtgärden CreateOrUpdate påbörjas.</span><span class="sxs-lookup"><span data-stu-id="09d17-918">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="09d17-919">0.4.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="09d17-919">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="09d17-920">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="09d17-920">Az.Profile</span></span>
* <span data-ttu-id="09d17-921">Åtgärdade problemet med Get-AzSubscription i CloudShell</span><span class="sxs-lookup"><span data-stu-id="09d17-921">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="09d17-922">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="09d17-922">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="09d17-923">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="09d17-923">Az.Compute</span></span>
* <span data-ttu-id="09d17-924">Nya storlekar lades till i listan över godkända VM-storlekar för vilka accelererat nätverk kommer att aktiveras vid användning av den enkla parameteruppsättningen för New-AzVm</span><span class="sxs-lookup"><span data-stu-id="09d17-924">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="09d17-925">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="09d17-925">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="09d17-926">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="09d17-926">Az.DataLakeStore</span></span>
* <span data-ttu-id="09d17-927">Lägger till stöd för regler för virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="09d17-927">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="09d17-928">Get-AzDataLakeStoreVirtualNetworkRule: Hämtar eller listar regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="09d17-928">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="09d17-929">Add-AzDataLakeStoreVirtualNetworkRule: Lägger till en regel för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="09d17-929">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="09d17-930">Set-AzDataLakeStoreVirtualNetworkRule: Ändrar den angivna regeln för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="09d17-930">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="09d17-931">Remove-AzDataLakeStoreVirtualNetworkRule: Tar bort en regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="09d17-931">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="09d17-932">Az.Network</span><span class="sxs-lookup"><span data-stu-id="09d17-932">Az.Network</span></span>
* <span data-ttu-id="09d17-933">Skicka protokollvärdet till serverdelen för att uppdatera cmdleten Test-AzNetworkWatcherConnectivity.</span><span class="sxs-lookup"><span data-stu-id="09d17-933">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="09d17-934">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="09d17-934">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="09d17-935">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="09d17-935">Az.Resources</span></span>
* <span data-ttu-id="09d17-936">Åtgärdade problem där Get-AzRoleDefinition genererar ett oläsligt undantag (när standardprofilen inte innehåller någon prenumeration och ingen omfattning har angetts) genom att lägga till ett beskrivande undantag i scenariot.</span><span class="sxs-lookup"><span data-stu-id="09d17-936">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="09d17-937">Ställ in ”RoleDefinitionNameParameterSet” som standardparameteruppsättning.</span><span class="sxs-lookup"><span data-stu-id="09d17-937">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="09d17-938">0.3.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="09d17-938">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="09d17-939">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="09d17-939">Azure.Storage</span></span>
* <span data-ttu-id="09d17-940">Åtgärda fel där Kopiera blob/fil inte kopierar metadata när målplatsen har ett problem med metadata</span><span class="sxs-lookup"><span data-stu-id="09d17-940">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="09d17-941">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="09d17-941">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="09d17-942">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="09d17-942">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="09d17-943">Stöd för att hämta användningsinformation om en Storage-resurs för en specifik plats och för att lägga till ett varningsmeddelande för att hämta användningsinformation om en global Storage-resurs är inaktuellt.</span><span class="sxs-lookup"><span data-stu-id="09d17-943">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="09d17-944">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="09d17-944">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="09d17-945">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="09d17-945">Az.CognitiveServices</span></span>
* <span data-ttu-id="09d17-946">Stöd för Get-AzCognitiveServicesAccountSkus utan ett befintligt konto.</span><span class="sxs-lookup"><span data-stu-id="09d17-946">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="09d17-947">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="09d17-947">Az.Compute</span></span>
* <span data-ttu-id="09d17-948">Åtgärdade fel där Get-AzVM -ResourceGroupName <rg> returnerar fler än 50 resultat om det behövs</span><span class="sxs-lookup"><span data-stu-id="09d17-948">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="09d17-949">Lade till ett exempel för SimpleParameterSet i hjälpen för cmdleten New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="09d17-949">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="09d17-950">Ett stavfel i förloppsmeddelandet för Azure Disk Encryption har korrigerats</span><span class="sxs-lookup"><span data-stu-id="09d17-950">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="09d17-951">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="09d17-951">Az.DataFactoryV2</span></span>
* <span data-ttu-id="09d17-952">ADF .Net SDK-versionen har uppdaterats till 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="09d17-952">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="09d17-953">Az.Network</span><span class="sxs-lookup"><span data-stu-id="09d17-953">Az.Network</span></span>
* <span data-ttu-id="09d17-954">Funktionalitet för NetworkProfile har lagts till.</span><span class="sxs-lookup"><span data-stu-id="09d17-954">Added NetworkProfile functionality.</span></span> <span data-ttu-id="09d17-955">nya cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="09d17-955">new cmdlets added</span></span>
    - <span data-ttu-id="09d17-956">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="09d17-956">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="09d17-957">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="09d17-957">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="09d17-958">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="09d17-958">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="09d17-959">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="09d17-959">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="09d17-960">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="09d17-960">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="09d17-961">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="09d17-961">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="09d17-962">Länk för tjänstassociering på modell för undernät har lagts till</span><span class="sxs-lookup"><span data-stu-id="09d17-962">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="09d17-963">Cmdletarna New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap och Remove-AzVirtualNetworkTap har lagts till</span><span class="sxs-lookup"><span data-stu-id="09d17-963">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="09d17-964">Cmdletarna Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig och Remove-AzNEtworkInterfaceTapConfig har lagts till</span><span class="sxs-lookup"><span data-stu-id="09d17-964">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="09d17-965">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="09d17-965">Az.RedisCache</span></span>
* <span data-ttu-id="09d17-966">Tillåt att alla strängar används som storleksparametrar framöver.</span><span class="sxs-lookup"><span data-stu-id="09d17-966">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="09d17-967">Lägg till P5 i popup-fönstret PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="09d17-967">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="09d17-968">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="09d17-968">Az.Resources</span></span>
* <span data-ttu-id="09d17-969">Parametern -Mode som saknades i Set-AzPolicyDefinition har lagts till</span><span class="sxs-lookup"><span data-stu-id="09d17-969">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="09d17-970">Åtgärdade buggen för cmdleten Get-AzProviderOperation för åtgärder med ursprung som innehåller användare</span><span class="sxs-lookup"><span data-stu-id="09d17-970">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="09d17-971">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="09d17-971">Az.Sql</span></span>
* <span data-ttu-id="09d17-972">Ett problem där vissa cmdletar för säkerhetskopiering inte kunde identifiera den aktuella azure-prenumerationen har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="09d17-972">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="09d17-973">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="09d17-973">Az.Websites</span></span>
* <span data-ttu-id="09d17-974">Ny cmdlet: Get-AzWebAppContainerContinuousDeploymentUrl – Hämtar webhook-URL:en för kontinuerlig distribution av container</span><span class="sxs-lookup"><span data-stu-id="09d17-974">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="09d17-975">Nya cmdletar: New-AzWebAppContainerPSSession och Enter-WebAppContainerPSSession – Startar en PowerShell-fjärrsession i en containerapp för windows</span><span class="sxs-lookup"><span data-stu-id="09d17-975">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="09d17-976">0.2.0 – september 2018</span><span class="sxs-lookup"><span data-stu-id="09d17-976">0.2.0 - September 2018</span></span>
 <span data-ttu-id="09d17-977">Första versionen</span><span class="sxs-lookup"><span data-stu-id="09d17-977">Initial Release</span></span>