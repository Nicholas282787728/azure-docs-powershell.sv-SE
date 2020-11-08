---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 0120bd19d1c8930129796e47758bd9f91dccfd5d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102525"
---
# <span data-ttu-id="643b5-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="643b5-101">Set-AzWebApp</span></span>

## <span data-ttu-id="643b5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="643b5-102">SYNOPSIS</span></span>
<span data-ttu-id="643b5-103">Ändrar ett Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="643b5-103">Modifies an Azure Web App.</span></span>

## <span data-ttu-id="643b5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="643b5-104">SYNTAX</span></span>

### <span data-ttu-id="643b5-105">S</span><span class="sxs-lookup"><span data-stu-id="643b5-105">S1</span></span>
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

### <span data-ttu-id="643b5-106">S2</span><span class="sxs-lookup"><span data-stu-id="643b5-106">S2</span></span>
```
Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]
 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="643b5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="643b5-107">DESCRIPTION</span></span>
<span data-ttu-id="643b5-108">Cmdleten **set-AzWebApp** anger en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="643b5-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="643b5-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="643b5-109">EXAMPLES</span></span>

### <span data-ttu-id="643b5-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="643b5-110">Example 1</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="643b5-111">Det här kommandot ändrar det AppService-abonnemang som är kopplat till Web App-ContosoWebApp som är kopplat till resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="643b5-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="643b5-112">Använd länken för att lära dig mer om hur du ändrar AppService plan och vilka villkor som är associerade med den.</span><span class="sxs-lookup"><span data-stu-id="643b5-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="643b5-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="643b5-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="643b5-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="643b5-114">Example 2</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="643b5-115">Det här kommandot anger HttpLoggingEnabled till sant för Web App-ContosoWebApp som är kopplat till resurs gruppens standard-väst</span><span class="sxs-lookup"><span data-stu-id="643b5-115">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

### <span data-ttu-id="643b5-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="643b5-116">Example 3</span></span>

<span data-ttu-id="643b5-117">Ändrar ett Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="643b5-117">Modifies an Azure Web App.</span></span> <span data-ttu-id="643b5-118">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="643b5-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzWebApp -AppSettings <Hashtable> -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS'
```

## <span data-ttu-id="643b5-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="643b5-119">PARAMETERS</span></span>

### <span data-ttu-id="643b5-120">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="643b5-120">-AlwaysOn</span></span>
<span data-ttu-id="643b5-121">Se till att webb programmet läses in hela tiden, i stället är inaktiverat.</span><span class="sxs-lookup"><span data-stu-id="643b5-121">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="643b5-122">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="643b5-122">-AppServicePlan</span></span>
<span data-ttu-id="643b5-123">Namn på App Service-abonnemang</span><span class="sxs-lookup"><span data-stu-id="643b5-123">App Service Plan Name</span></span>

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

### <span data-ttu-id="643b5-124">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="643b5-124">-AppSettings</span></span>
<span data-ttu-id="643b5-125">App Settings-hash.</span><span class="sxs-lookup"><span data-stu-id="643b5-125">App Settings HashTable.</span></span> <span data-ttu-id="643b5-126">Befintliga program inställningar ersätts och tar bort alla inställningar som inte tillhandahålls.</span><span class="sxs-lookup"><span data-stu-id="643b5-126">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="643b5-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="643b5-127">-AsJob</span></span>
<span data-ttu-id="643b5-128">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="643b5-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="643b5-129">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="643b5-129">-AssignIdentity</span></span>
<span data-ttu-id="643b5-130">Aktivera/inaktivera MSI på en befintlig Azure webapp eller functionapp</span><span class="sxs-lookup"><span data-stu-id="643b5-130">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="643b5-131">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="643b5-131">-AutoSwapSlotName</span></span>
<span data-ttu-id="643b5-132">Mål plats namn för automatisk växling</span><span class="sxs-lookup"><span data-stu-id="643b5-132">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="643b5-133">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="643b5-133">-AzureStoragePath</span></span>
<span data-ttu-id="643b5-134">Azure-lagring för montering i en Web App för container.</span><span class="sxs-lookup"><span data-stu-id="643b5-134">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="643b5-135">Använda New-AzureRmWebAppAzureStoragePath för att skapa den</span><span class="sxs-lookup"><span data-stu-id="643b5-135">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="643b5-136">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="643b5-136">-ConnectionStrings</span></span>
<span data-ttu-id="643b5-137">Anslutnings strängar-hash</span><span class="sxs-lookup"><span data-stu-id="643b5-137">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="643b5-138">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="643b5-138">-ContainerImageName</span></span>
<span data-ttu-id="643b5-139">Bild namn för behållare</span><span class="sxs-lookup"><span data-stu-id="643b5-139">Container Image Name</span></span>

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

### <span data-ttu-id="643b5-140">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="643b5-140">-ContainerRegistryPassword</span></span>
<span data-ttu-id="643b5-141">Lösen ord för privat behållare</span><span class="sxs-lookup"><span data-stu-id="643b5-141">Private Container Registry Password</span></span>

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

### <span data-ttu-id="643b5-142">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="643b5-142">-ContainerRegistryUrl</span></span>
<span data-ttu-id="643b5-143">Webb adress för privat behållarens register Server</span><span class="sxs-lookup"><span data-stu-id="643b5-143">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="643b5-144">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="643b5-144">-ContainerRegistryUser</span></span>
<span data-ttu-id="643b5-145">Användar namn för privat behållare</span><span class="sxs-lookup"><span data-stu-id="643b5-145">Private Container Registry Username</span></span>

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

### <span data-ttu-id="643b5-146">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="643b5-146">-DefaultDocuments</span></span>
<span data-ttu-id="643b5-147">Matris för standard dokument</span><span class="sxs-lookup"><span data-stu-id="643b5-147">Default Documents String Array</span></span>

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

### <span data-ttu-id="643b5-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="643b5-148">-DefaultProfile</span></span>
<span data-ttu-id="643b5-149">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="643b5-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="643b5-150">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="643b5-150">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="643b5-151">Detaljerad fel loggning aktiverat boolesk</span><span class="sxs-lookup"><span data-stu-id="643b5-151">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="643b5-152">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="643b5-152">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="643b5-153">Aktiverar/inaktiverar kontinuerlig distribution av behållare webhook</span><span class="sxs-lookup"><span data-stu-id="643b5-153">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="643b5-154">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="643b5-154">-FtpsState</span></span>
<span data-ttu-id="643b5-155">Ange FTPS tillstånds värde för ett program.</span><span class="sxs-lookup"><span data-stu-id="643b5-155">Set the Ftps state value for an app.</span></span> <span data-ttu-id="643b5-156">Tillåtna värden [AllAllowed | Disabled | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="643b5-156">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="643b5-157">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="643b5-157">-HandlerMappings</span></span>
<span data-ttu-id="643b5-158">Hanterar mappningar IList</span><span class="sxs-lookup"><span data-stu-id="643b5-158">Handler Mappings IList</span></span>

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

### <span data-ttu-id="643b5-159">-Värdnamn</span><span class="sxs-lookup"><span data-stu-id="643b5-159">-HostNames</span></span>
<span data-ttu-id="643b5-160">Matris för WebApp-värdnamn</span><span class="sxs-lookup"><span data-stu-id="643b5-160">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="643b5-161">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="643b5-161">-HttpLoggingEnabled</span></span>
<span data-ttu-id="643b5-162">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="643b5-162">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="643b5-163">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="643b5-163">-HttpsOnly</span></span>
<span data-ttu-id="643b5-164">Aktivera/inaktivera omdirigering av all trafik till HTTPS på en befintlig Azure webapp eller functionapp</span><span class="sxs-lookup"><span data-stu-id="643b5-164">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="643b5-165">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="643b5-165">-ManagedPipelineMode</span></span>
<span data-ttu-id="643b5-166">Namn på hanterat pipeline-läge</span><span class="sxs-lookup"><span data-stu-id="643b5-166">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="643b5-167">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="643b5-167">-MinTlsVersion</span></span>
<span data-ttu-id="643b5-168">Den minsta versionen av TLS som krävs för SSL-begäranden.</span><span class="sxs-lookup"><span data-stu-id="643b5-168">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="643b5-169">Tillåtna värden [1,0 | 1,1 | 1,2].</span><span class="sxs-lookup"><span data-stu-id="643b5-169">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="643b5-170">-Namn</span><span class="sxs-lookup"><span data-stu-id="643b5-170">-Name</span></span>
<span data-ttu-id="643b5-171">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="643b5-171">WebApp Name</span></span>

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

### <span data-ttu-id="643b5-172">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="643b5-172">-NetFrameworkVersion</span></span>
<span data-ttu-id="643b5-173">NET Framework-version</span><span class="sxs-lookup"><span data-stu-id="643b5-173">Net Framework Version</span></span>

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

### <span data-ttu-id="643b5-174">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="643b5-174">-NumberOfWorkers</span></span>
<span data-ttu-id="643b5-175">Antalet arbetare som ska tilldelas</span><span class="sxs-lookup"><span data-stu-id="643b5-175">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="643b5-176">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="643b5-176">-PhpVersion</span></span>
<span data-ttu-id="643b5-177">Php-version</span><span class="sxs-lookup"><span data-stu-id="643b5-177">Php Version</span></span>

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

### <span data-ttu-id="643b5-178">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="643b5-178">-RequestTracingEnabled</span></span>
<span data-ttu-id="643b5-179">Begäran om spårning aktive rad</span><span class="sxs-lookup"><span data-stu-id="643b5-179">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="643b5-180">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="643b5-180">-ResourceGroupName</span></span>
<span data-ttu-id="643b5-181">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="643b5-181">Resource Group Name</span></span>

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

### <span data-ttu-id="643b5-182">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="643b5-182">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="643b5-183">Använda 32-bitars boolesk arbets process</span><span class="sxs-lookup"><span data-stu-id="643b5-183">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="643b5-184">-WebApp</span><span class="sxs-lookup"><span data-stu-id="643b5-184">-WebApp</span></span>
<span data-ttu-id="643b5-185">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="643b5-185">WebApp Object</span></span>

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

### <span data-ttu-id="643b5-186">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="643b5-186">-WebSocketsEnabled</span></span>
<span data-ttu-id="643b5-187">WebSocketsEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="643b5-187">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="643b5-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="643b5-188">CommonParameters</span></span>
<span data-ttu-id="643b5-189">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="643b5-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="643b5-190">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="643b5-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="643b5-191">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="643b5-191">INPUTS</span></span>

### <span data-ttu-id="643b5-192">System. Int32</span><span class="sxs-lookup"><span data-stu-id="643b5-192">System.Int32</span></span>

### <span data-ttu-id="643b5-193">System. String</span><span class="sxs-lookup"><span data-stu-id="643b5-193">System.String</span></span>

### <span data-ttu-id="643b5-194">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="643b5-194">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="643b5-195">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="643b5-195">OUTPUTS</span></span>

### <span data-ttu-id="643b5-196">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="643b5-196">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="643b5-197">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="643b5-197">NOTES</span></span>
<span data-ttu-id="643b5-198">Under angiven cmdlet kan du uppdatera Azure Web App till **DOTNETCORE**</span><span class="sxs-lookup"><span data-stu-id="643b5-198">Below provided cmdlet will help you to update Azure Web App to **DOTNETCORE**</span></span>

<span data-ttu-id="643b5-199">$PropertiesObject = @ {"CURRENT_STACK" = "dotnetcore"} New-AzResource-PropertyObject $PropertiesObject-ResourceGroupName "default-Web-West"-ResourceType Microsoft. Web/Sites/config-ResourceName "ContosoWebApp/metadata" – ApiVersion 2018-02-01-Force</span><span class="sxs-lookup"><span data-stu-id="643b5-199">$PropertiesObject = @{ "CURRENT_STACK" =  "dotnetcore" } New-AzResource -PropertyObject $PropertiesObject -ResourceGroupName "Default-Web-WestUS" -ResourceType Microsoft.Web/sites/config -ResourceName "ContosoWebApp/metadata" -ApiVersion 2018-02-01 -Force</span></span>

<span data-ttu-id="643b5-200">Ersätt värdena som standard-väst med ditt resurs grupp namn för webapp and ContosoWebApp med webapp-namnet.</span><span class="sxs-lookup"><span data-stu-id="643b5-200">Replace the values of Default-Web-WestUS with your resource group name of the webapp and ContosoWebApp with the webapp name.</span></span>
 
## <span data-ttu-id="643b5-201">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="643b5-201">RELATED LINKS</span></span>

[<span data-ttu-id="643b5-202">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="643b5-202">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="643b5-203">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="643b5-203">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="643b5-204">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="643b5-204">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="643b5-205">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="643b5-205">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="643b5-206">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="643b5-206">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="643b5-207">Stopp-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="643b5-207">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)

[<span data-ttu-id="643b5-208">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="643b5-208">New-AzResource</span></span>](./New-AzResource.md)
