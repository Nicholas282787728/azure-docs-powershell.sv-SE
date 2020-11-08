---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 75ee07a9ce74f5b2667d8197ca141883508faa1e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090628"
---
# <span data-ttu-id="33d68-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="33d68-101">Set-AzWebApp</span></span>

## <span data-ttu-id="33d68-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="33d68-102">SYNOPSIS</span></span>
<span data-ttu-id="33d68-103">Ändrar ett Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="33d68-103">Modifies an Azure Web App.</span></span>

## <span data-ttu-id="33d68-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="33d68-104">SYNTAX</span></span>

### <span data-ttu-id="33d68-105">S</span><span class="sxs-lookup"><span data-stu-id="33d68-105">S1</span></span>
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
 [-AlwaysOn <Boolean>] [-MinTlsVersion <String>] [-FtpsState <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33d68-106">S2</span><span class="sxs-lookup"><span data-stu-id="33d68-106">S2</span></span>
```
Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]
 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33d68-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="33d68-107">DESCRIPTION</span></span>
<span data-ttu-id="33d68-108">Cmdleten **set-AzWebApp** anger en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="33d68-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="33d68-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="33d68-109">EXAMPLES</span></span>

### <span data-ttu-id="33d68-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="33d68-110">Example 1</span></span>
```
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="33d68-111">Det här kommandot ändrar det AppService-abonnemang som är kopplat till Web App-ContosoWebApp som är kopplat till resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="33d68-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="33d68-112">Använd länken för att lära dig mer om hur du ändrar AppService plan och vilka villkor som är associerade med den.</span><span class="sxs-lookup"><span data-stu-id="33d68-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="33d68-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="33d68-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="33d68-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="33d68-114">Example 2</span></span>
```
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="33d68-115">Det här kommandot anger HttpLoggingEnabled till sant för Web App-ContosoWebApp som är kopplat till resurs gruppens standard-väst</span><span class="sxs-lookup"><span data-stu-id="33d68-115">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="33d68-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="33d68-116">PARAMETERS</span></span>

### <span data-ttu-id="33d68-117">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="33d68-117">-AlwaysOn</span></span>
<span data-ttu-id="33d68-118">Se till att webb programmet läses in hela tiden, i stället är inaktiverat.</span><span class="sxs-lookup"><span data-stu-id="33d68-118">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="33d68-119">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="33d68-119">-AppServicePlan</span></span>
<span data-ttu-id="33d68-120">Namn på App Service-abonnemang</span><span class="sxs-lookup"><span data-stu-id="33d68-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="33d68-121">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="33d68-121">-AppSettings</span></span>
<span data-ttu-id="33d68-122">App Settings-hash.</span><span class="sxs-lookup"><span data-stu-id="33d68-122">App Settings HashTable.</span></span> <span data-ttu-id="33d68-123">Befintliga program inställningar ersätts och tar bort alla inställningar som inte tillhandahålls.</span><span class="sxs-lookup"><span data-stu-id="33d68-123">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="33d68-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="33d68-124">-AsJob</span></span>
<span data-ttu-id="33d68-125">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="33d68-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="33d68-126">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="33d68-126">-AssignIdentity</span></span>
<span data-ttu-id="33d68-127">Aktivera/inaktivera MSI på en befintlig Azure webapp eller functionapp</span><span class="sxs-lookup"><span data-stu-id="33d68-127">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="33d68-128">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="33d68-128">-AutoSwapSlotName</span></span>
<span data-ttu-id="33d68-129">Mål plats namn för automatisk växling</span><span class="sxs-lookup"><span data-stu-id="33d68-129">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="33d68-130">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="33d68-130">-AzureStoragePath</span></span>
<span data-ttu-id="33d68-131">Azure-lagring för montering i en Web App för container.</span><span class="sxs-lookup"><span data-stu-id="33d68-131">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="33d68-132">Använda New-AzureRmWebAppAzureStoragePath för att skapa den</span><span class="sxs-lookup"><span data-stu-id="33d68-132">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="33d68-133">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="33d68-133">-ConnectionStrings</span></span>
<span data-ttu-id="33d68-134">Anslutnings strängar-hash</span><span class="sxs-lookup"><span data-stu-id="33d68-134">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="33d68-135">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="33d68-135">-ContainerImageName</span></span>
<span data-ttu-id="33d68-136">Bild namn för behållare</span><span class="sxs-lookup"><span data-stu-id="33d68-136">Container Image Name</span></span>

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

### <span data-ttu-id="33d68-137">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="33d68-137">-ContainerRegistryPassword</span></span>
<span data-ttu-id="33d68-138">Lösen ord för privat behållare</span><span class="sxs-lookup"><span data-stu-id="33d68-138">Private Container Registry Password</span></span>

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

### <span data-ttu-id="33d68-139">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="33d68-139">-ContainerRegistryUrl</span></span>
<span data-ttu-id="33d68-140">Webb adress för privat behållarens register Server</span><span class="sxs-lookup"><span data-stu-id="33d68-140">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="33d68-141">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="33d68-141">-ContainerRegistryUser</span></span>
<span data-ttu-id="33d68-142">Användar namn för privat behållare</span><span class="sxs-lookup"><span data-stu-id="33d68-142">Private Container Registry Username</span></span>

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

### <span data-ttu-id="33d68-143">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="33d68-143">-DefaultDocuments</span></span>
<span data-ttu-id="33d68-144">Matris för standard dokument</span><span class="sxs-lookup"><span data-stu-id="33d68-144">Default Documents String Array</span></span>

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

### <span data-ttu-id="33d68-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33d68-145">-DefaultProfile</span></span>
<span data-ttu-id="33d68-146">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="33d68-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33d68-147">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="33d68-147">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="33d68-148">Detaljerad fel loggning aktiverat boolesk</span><span class="sxs-lookup"><span data-stu-id="33d68-148">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="33d68-149">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="33d68-149">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="33d68-150">Aktiverar/inaktiverar kontinuerlig distribution av behållare webhook</span><span class="sxs-lookup"><span data-stu-id="33d68-150">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="33d68-151">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="33d68-151">-FtpsState</span></span>
<span data-ttu-id="33d68-152">Ange FTPS tillstånds värde för ett program.</span><span class="sxs-lookup"><span data-stu-id="33d68-152">Set the Ftps state value for an app.</span></span> <span data-ttu-id="33d68-153">Tillåtna värden [AllAllowed | Disabled | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="33d68-153">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="33d68-154">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="33d68-154">-HandlerMappings</span></span>
<span data-ttu-id="33d68-155">Hanterar mappningar IList</span><span class="sxs-lookup"><span data-stu-id="33d68-155">Handler Mappings IList</span></span>

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

### <span data-ttu-id="33d68-156">-Värdnamn</span><span class="sxs-lookup"><span data-stu-id="33d68-156">-HostNames</span></span>
<span data-ttu-id="33d68-157">Matris för WebApp-värdnamn</span><span class="sxs-lookup"><span data-stu-id="33d68-157">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="33d68-158">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="33d68-158">-HttpLoggingEnabled</span></span>
<span data-ttu-id="33d68-159">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="33d68-159">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="33d68-160">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="33d68-160">-HttpsOnly</span></span>
<span data-ttu-id="33d68-161">Aktivera/inaktivera omdirigering av all trafik till HTTPS på en befintlig Azure webapp eller functionapp</span><span class="sxs-lookup"><span data-stu-id="33d68-161">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="33d68-162">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="33d68-162">-ManagedPipelineMode</span></span>
<span data-ttu-id="33d68-163">Namn på hanterat pipeline-läge</span><span class="sxs-lookup"><span data-stu-id="33d68-163">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="33d68-164">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="33d68-164">-MinTlsVersion</span></span>
<span data-ttu-id="33d68-165">Den minsta versionen av TLS som krävs för SSL-begäranden.</span><span class="sxs-lookup"><span data-stu-id="33d68-165">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="33d68-166">Tillåtna värden [1,0 | 1,1 | 1,2].</span><span class="sxs-lookup"><span data-stu-id="33d68-166">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="33d68-167">-Namn</span><span class="sxs-lookup"><span data-stu-id="33d68-167">-Name</span></span>
<span data-ttu-id="33d68-168">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="33d68-168">WebApp Name</span></span>

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

### <span data-ttu-id="33d68-169">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="33d68-169">-NetFrameworkVersion</span></span>
<span data-ttu-id="33d68-170">NET Framework-version</span><span class="sxs-lookup"><span data-stu-id="33d68-170">Net Framework Version</span></span>

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

### <span data-ttu-id="33d68-171">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="33d68-171">-NumberOfWorkers</span></span>
<span data-ttu-id="33d68-172">Antalet arbetare som ska tilldelas</span><span class="sxs-lookup"><span data-stu-id="33d68-172">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="33d68-173">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="33d68-173">-PhpVersion</span></span>
<span data-ttu-id="33d68-174">Php-version</span><span class="sxs-lookup"><span data-stu-id="33d68-174">Php Version</span></span>

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

### <span data-ttu-id="33d68-175">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="33d68-175">-RequestTracingEnabled</span></span>
<span data-ttu-id="33d68-176">Begäran om spårning aktive rad</span><span class="sxs-lookup"><span data-stu-id="33d68-176">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="33d68-177">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33d68-177">-ResourceGroupName</span></span>
<span data-ttu-id="33d68-178">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="33d68-178">Resource Group Name</span></span>

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

### <span data-ttu-id="33d68-179">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="33d68-179">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="33d68-180">Använda 32-bitars boolesk arbets process</span><span class="sxs-lookup"><span data-stu-id="33d68-180">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="33d68-181">-WebApp</span><span class="sxs-lookup"><span data-stu-id="33d68-181">-WebApp</span></span>
<span data-ttu-id="33d68-182">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="33d68-182">WebApp Object</span></span>

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

### <span data-ttu-id="33d68-183">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="33d68-183">-WebSocketsEnabled</span></span>
<span data-ttu-id="33d68-184">WebSocketsEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="33d68-184">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="33d68-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33d68-185">CommonParameters</span></span>
<span data-ttu-id="33d68-186">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33d68-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33d68-187">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="33d68-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33d68-188">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="33d68-188">INPUTS</span></span>

### <span data-ttu-id="33d68-189">System. Int32</span><span class="sxs-lookup"><span data-stu-id="33d68-189">System.Int32</span></span>

### <span data-ttu-id="33d68-190">System. String</span><span class="sxs-lookup"><span data-stu-id="33d68-190">System.String</span></span>

### <span data-ttu-id="33d68-191">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="33d68-191">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="33d68-192">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="33d68-192">OUTPUTS</span></span>

### <span data-ttu-id="33d68-193">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="33d68-193">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="33d68-194">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="33d68-194">NOTES</span></span>

## <span data-ttu-id="33d68-195">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="33d68-195">RELATED LINKS</span></span>

[<span data-ttu-id="33d68-196">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="33d68-196">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="33d68-197">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="33d68-197">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="33d68-198">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="33d68-198">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="33d68-199">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="33d68-199">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="33d68-200">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="33d68-200">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="33d68-201">Stopp-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="33d68-201">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)
