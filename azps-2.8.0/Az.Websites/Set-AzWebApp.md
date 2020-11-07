---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 4e4e842605b883b97d408d36929bedc5fef21e4b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920914"
---
# <span data-ttu-id="913f1-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="913f1-101">Set-AzWebApp</span></span>

## <span data-ttu-id="913f1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="913f1-102">SYNOPSIS</span></span>
<span data-ttu-id="913f1-103">Ändrar ett Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="913f1-103">Modifies an Azure Web App.</span></span>

## <span data-ttu-id="913f1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="913f1-104">SYNTAX</span></span>

### <span data-ttu-id="913f1-105">S</span><span class="sxs-lookup"><span data-stu-id="913f1-105">S1</span></span>
```
Set-AzWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>] [[-NetFrameworkVersion] <String>]
 [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>] [[-HttpLoggingEnabled] <Boolean>]
 [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>] [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [[-AutoSwapSlotName] <String>] [-ContainerImageName <String>] [-ContainerRegistryUrl <String>]
 [-ContainerRegistryUser <String>] [-ContainerRegistryPassword <SecureString>]
 [-EnableContainerContinuousDeployment <Boolean>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>] [-AsJob]
 [-AssignIdentity <Boolean>] [-HttpsOnly <Boolean>] [-AzureStoragePath <WebAppAzureStoragePath[]>]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="913f1-106">S2</span><span class="sxs-lookup"><span data-stu-id="913f1-106">S2</span></span>
```
Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]
 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="913f1-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="913f1-107">DESCRIPTION</span></span>
<span data-ttu-id="913f1-108">Cmdleten **set-AzWebApp** anger en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="913f1-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="913f1-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="913f1-109">EXAMPLES</span></span>

### <span data-ttu-id="913f1-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="913f1-110">Example 1</span></span>
```
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="913f1-111">Det här kommandot ändrar det AppService-abonnemang som är kopplat till Web App-ContosoWebApp som är kopplat till resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="913f1-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="913f1-112">Använd länken för att lära dig mer om hur du ändrar AppService plan och vilka villkor som är associerade med den.</span><span class="sxs-lookup"><span data-stu-id="913f1-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="913f1-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="913f1-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="913f1-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="913f1-114">Example 2</span></span>
```
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="913f1-115">Det här kommandot anger HttpLoggingEnabled till sant för Web App-ContosoWebApp som är kopplat till resurs gruppens standard-väst</span><span class="sxs-lookup"><span data-stu-id="913f1-115">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="913f1-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="913f1-116">PARAMETERS</span></span>

### <span data-ttu-id="913f1-117">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="913f1-117">-AppServicePlan</span></span>
<span data-ttu-id="913f1-118">Namn på App Service-abonnemang</span><span class="sxs-lookup"><span data-stu-id="913f1-118">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="913f1-119">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="913f1-119">-AppSettings</span></span>
<span data-ttu-id="913f1-120">App Settings-hash.</span><span class="sxs-lookup"><span data-stu-id="913f1-120">App Settings HashTable.</span></span> <span data-ttu-id="913f1-121">Befintliga program inställningar ersätts och tar bort alla inställningar som inte tillhandahålls.</span><span class="sxs-lookup"><span data-stu-id="913f1-121">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: S1
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="913f1-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="913f1-122">-AsJob</span></span>
<span data-ttu-id="913f1-123">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="913f1-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="913f1-124">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="913f1-124">-AssignIdentity</span></span>
<span data-ttu-id="913f1-125">Aktivera/inaktivera MSI på en befintlig Azure webapp eller functionapp</span><span class="sxs-lookup"><span data-stu-id="913f1-125">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="913f1-126">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="913f1-126">-AutoSwapSlotName</span></span>
<span data-ttu-id="913f1-127">Mål plats namn för automatisk växling</span><span class="sxs-lookup"><span data-stu-id="913f1-127">Destination slot name for auto swap</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 15
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="913f1-128">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="913f1-128">-AzureStoragePath</span></span>
<span data-ttu-id="913f1-129">Azure-lagring för montering i en Web App för container.</span><span class="sxs-lookup"><span data-stu-id="913f1-129">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="913f1-130">Använda New-AzureRmWebAppAzureStoragePath för att skapa den</span><span class="sxs-lookup"><span data-stu-id="913f1-130">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebAppAzureStoragePath[]
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="913f1-131">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="913f1-131">-ConnectionStrings</span></span>
<span data-ttu-id="913f1-132">Anslutnings strängar-hash</span><span class="sxs-lookup"><span data-stu-id="913f1-132">Connection Strings HashTable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: S1
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="913f1-133">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="913f1-133">-ContainerImageName</span></span>
<span data-ttu-id="913f1-134">Bild namn för behållare</span><span class="sxs-lookup"><span data-stu-id="913f1-134">Container Image Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="913f1-135">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="913f1-135">-ContainerRegistryPassword</span></span>
<span data-ttu-id="913f1-136">Lösen ord för privat behållare</span><span class="sxs-lookup"><span data-stu-id="913f1-136">Private Container Registry Password</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="913f1-137">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="913f1-137">-ContainerRegistryUrl</span></span>
<span data-ttu-id="913f1-138">Webb adress för privat behållarens register Server</span><span class="sxs-lookup"><span data-stu-id="913f1-138">Private Container Registry Server Url</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="913f1-139">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="913f1-139">-ContainerRegistryUser</span></span>
<span data-ttu-id="913f1-140">Användar namn för privat behållare</span><span class="sxs-lookup"><span data-stu-id="913f1-140">Private Container Registry Username</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="913f1-141">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="913f1-141">-DefaultDocuments</span></span>
<span data-ttu-id="913f1-142">Matris för standard dokument</span><span class="sxs-lookup"><span data-stu-id="913f1-142">Default Documents String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: S1
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="913f1-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="913f1-143">-DefaultProfile</span></span>
<span data-ttu-id="913f1-144">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="913f1-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="913f1-145">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="913f1-145">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="913f1-146">Detaljerad fel loggning aktiverat boolesk</span><span class="sxs-lookup"><span data-stu-id="913f1-146">Detailed Error Logging Enabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="913f1-147">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="913f1-147">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="913f1-148">Aktiverar/inaktiverar kontinuerlig distribution av behållare webhook</span><span class="sxs-lookup"><span data-stu-id="913f1-148">Enables/Disables container continuous deployment webhook</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="913f1-149">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="913f1-149">-HandlerMappings</span></span>
<span data-ttu-id="913f1-150">Hanterar mappningar IList</span><span class="sxs-lookup"><span data-stu-id="913f1-150">Handler Mappings IList</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]
Parameter Sets: S1
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="913f1-151">-Värdnamn</span><span class="sxs-lookup"><span data-stu-id="913f1-151">-HostNames</span></span>
<span data-ttu-id="913f1-152">Matris för WebApp-värdnamn</span><span class="sxs-lookup"><span data-stu-id="913f1-152">WebApp HostNames String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="913f1-153">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="913f1-153">-HttpLoggingEnabled</span></span>
<span data-ttu-id="913f1-154">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="913f1-154">HttpLoggingEnabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="913f1-155">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="913f1-155">-HttpsOnly</span></span>
<span data-ttu-id="913f1-156">Aktivera/inaktivera omdirigering av all trafik till HTTPS på en befintlig Azure webapp eller functionapp</span><span class="sxs-lookup"><span data-stu-id="913f1-156">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="913f1-157">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="913f1-157">-ManagedPipelineMode</span></span>
<span data-ttu-id="913f1-158">Namn på hanterat pipeline-läge</span><span class="sxs-lookup"><span data-stu-id="913f1-158">Managed Pipeline Mode Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:
Accepted values: Classic, Integrated

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="913f1-159">-Namn</span><span class="sxs-lookup"><span data-stu-id="913f1-159">-Name</span></span>
<span data-ttu-id="913f1-160">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="913f1-160">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="913f1-161">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="913f1-161">-NetFrameworkVersion</span></span>
<span data-ttu-id="913f1-162">NET Framework-version</span><span class="sxs-lookup"><span data-stu-id="913f1-162">Net Framework Version</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="913f1-163">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="913f1-163">-NumberOfWorkers</span></span>
<span data-ttu-id="913f1-164">Antalet arbetare som ska tilldelas</span><span class="sxs-lookup"><span data-stu-id="913f1-164">The number of workers to be allocated</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="913f1-165">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="913f1-165">-PhpVersion</span></span>
<span data-ttu-id="913f1-166">Php-version</span><span class="sxs-lookup"><span data-stu-id="913f1-166">Php Version</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="913f1-167">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="913f1-167">-RequestTracingEnabled</span></span>
<span data-ttu-id="913f1-168">Begäran om spårning aktive rad</span><span class="sxs-lookup"><span data-stu-id="913f1-168">Request Tracing Enabled</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="913f1-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="913f1-169">-ResourceGroupName</span></span>
<span data-ttu-id="913f1-170">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="913f1-170">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="913f1-171">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="913f1-171">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="913f1-172">Använda 32-bitars boolesk arbets process</span><span class="sxs-lookup"><span data-stu-id="913f1-172">Use 32-bit Worker Process Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 14
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="913f1-173">-WebApp</span><span class="sxs-lookup"><span data-stu-id="913f1-173">-WebApp</span></span>
<span data-ttu-id="913f1-174">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="913f1-174">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="913f1-175">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="913f1-175">-WebSocketsEnabled</span></span>
<span data-ttu-id="913f1-176">WebSocketsEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="913f1-176">WebSocketsEnabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="913f1-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="913f1-177">CommonParameters</span></span>
<span data-ttu-id="913f1-178">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="913f1-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="913f1-179">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="913f1-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="913f1-180">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="913f1-180">INPUTS</span></span>

### <span data-ttu-id="913f1-181">System. Int32</span><span class="sxs-lookup"><span data-stu-id="913f1-181">System.Int32</span></span>

### <span data-ttu-id="913f1-182">System. String</span><span class="sxs-lookup"><span data-stu-id="913f1-182">System.String</span></span>

### <span data-ttu-id="913f1-183">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="913f1-183">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="913f1-184">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="913f1-184">OUTPUTS</span></span>

### <span data-ttu-id="913f1-185">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="913f1-185">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="913f1-186">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="913f1-186">NOTES</span></span>

## <span data-ttu-id="913f1-187">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="913f1-187">RELATED LINKS</span></span>

[<span data-ttu-id="913f1-188">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="913f1-188">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="913f1-189">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="913f1-189">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="913f1-190">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="913f1-190">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="913f1-191">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="913f1-191">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="913f1-192">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="913f1-192">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="913f1-193">Stopp-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="913f1-193">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)
