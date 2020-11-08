---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 2028132e427bdba3fd49c20b9e7944eff90a9aa5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272367"
---
# <span data-ttu-id="9c3b1-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="9c3b1-101">Set-AzWebApp</span></span>

## <span data-ttu-id="9c3b1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9c3b1-102">SYNOPSIS</span></span>
<span data-ttu-id="9c3b1-103">Ändrar ett Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="9c3b1-103">Modifies an Azure Web App.</span></span>

## <span data-ttu-id="9c3b1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9c3b1-104">SYNTAX</span></span>

### <span data-ttu-id="9c3b1-105">S</span><span class="sxs-lookup"><span data-stu-id="9c3b1-105">S1</span></span>
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

### <span data-ttu-id="9c3b1-106">S2</span><span class="sxs-lookup"><span data-stu-id="9c3b1-106">S2</span></span>
```
Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]
 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c3b1-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9c3b1-107">DESCRIPTION</span></span>
<span data-ttu-id="9c3b1-108">Cmdleten **set-AzWebApp** anger en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="9c3b1-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="9c3b1-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9c3b1-109">EXAMPLES</span></span>

### <span data-ttu-id="9c3b1-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9c3b1-110">Example 1</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="9c3b1-111">Det här kommandot ändrar det AppService-abonnemang som är kopplat till Web App-ContosoWebApp som är kopplat till resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="9c3b1-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="9c3b1-112">Använd länken för att lära dig mer om hur du ändrar AppService plan och vilka villkor som är associerade med den.</span><span class="sxs-lookup"><span data-stu-id="9c3b1-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="9c3b1-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="9c3b1-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="9c3b1-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="9c3b1-114">Example 2</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="9c3b1-115">Det här kommandot anger HttpLoggingEnabled till sant för Web App-ContosoWebApp som är kopplat till resurs gruppens standard-väst</span><span class="sxs-lookup"><span data-stu-id="9c3b1-115">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

### <span data-ttu-id="9c3b1-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="9c3b1-116">Example 3</span></span>

<span data-ttu-id="9c3b1-117">Ändrar ett Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="9c3b1-117">Modifies an Azure Web App.</span></span> <span data-ttu-id="9c3b1-118">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="9c3b1-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzWebApp -AppSettings <Hashtable> -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS'
```

### <span data-ttu-id="9c3b1-119">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="9c3b1-119">Example 4</span></span>

<span data-ttu-id="9c3b1-120">I följande exempel skapas en anslutnings sträng som heter ' ConnectionString för Web App ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="9c3b1-120">The following example creates a connection string named myConnectionString for Web App ContosoWebApp.</span></span> <span data-ttu-id="9c3b1-121">Detta ersätter alla befintliga anslutnings strängar för Web App-ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="9c3b1-121">This replaces all existing connection strings for Web App ContosoWebApp.</span></span>

```powershell
$hashtable =  @{myConnectionString = @{Type='MySql';Value='MySql Connection string'}}
Set-AzWebApp -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS' -ConnectionString $hashtable
```

## <span data-ttu-id="9c3b1-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9c3b1-122">PARAMETERS</span></span>

### <span data-ttu-id="9c3b1-123">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="9c3b1-123">-AlwaysOn</span></span>
<span data-ttu-id="9c3b1-124">Se till att webb programmet läses in hela tiden, i stället är inaktiverat.</span><span class="sxs-lookup"><span data-stu-id="9c3b1-124">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="9c3b1-125">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9c3b1-125">-AppServicePlan</span></span>
<span data-ttu-id="9c3b1-126">Namn på App Service-abonnemang</span><span class="sxs-lookup"><span data-stu-id="9c3b1-126">App Service Plan Name</span></span>

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

### <span data-ttu-id="9c3b1-127">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="9c3b1-127">-AppSettings</span></span>
<span data-ttu-id="9c3b1-128">App Settings-hash.</span><span class="sxs-lookup"><span data-stu-id="9c3b1-128">App Settings HashTable.</span></span> <span data-ttu-id="9c3b1-129">Befintliga program inställningar ersätts och tar bort alla inställningar som inte tillhandahålls.</span><span class="sxs-lookup"><span data-stu-id="9c3b1-129">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="9c3b1-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9c3b1-130">-AsJob</span></span>
<span data-ttu-id="9c3b1-131">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="9c3b1-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9c3b1-132">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="9c3b1-132">-AssignIdentity</span></span>
<span data-ttu-id="9c3b1-133">Aktivera/inaktivera MSI på en befintlig Azure webapp eller functionapp</span><span class="sxs-lookup"><span data-stu-id="9c3b1-133">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="9c3b1-134">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="9c3b1-134">-AutoSwapSlotName</span></span>
<span data-ttu-id="9c3b1-135">Mål plats namn för automatisk växling</span><span class="sxs-lookup"><span data-stu-id="9c3b1-135">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="9c3b1-136">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="9c3b1-136">-AzureStoragePath</span></span>
<span data-ttu-id="9c3b1-137">Azure-lagring för montering i en Web App för container.</span><span class="sxs-lookup"><span data-stu-id="9c3b1-137">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="9c3b1-138">Använda New-AzureRmWebAppAzureStoragePath för att skapa den</span><span class="sxs-lookup"><span data-stu-id="9c3b1-138">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="9c3b1-139">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="9c3b1-139">-ConnectionStrings</span></span>
<span data-ttu-id="9c3b1-140">Anslutnings strängar-hash</span><span class="sxs-lookup"><span data-stu-id="9c3b1-140">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="9c3b1-141">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="9c3b1-141">-ContainerImageName</span></span>
<span data-ttu-id="9c3b1-142">Bild namn för behållare</span><span class="sxs-lookup"><span data-stu-id="9c3b1-142">Container Image Name</span></span>

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

### <span data-ttu-id="9c3b1-143">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="9c3b1-143">-ContainerRegistryPassword</span></span>
<span data-ttu-id="9c3b1-144">Lösen ord för privat behållare</span><span class="sxs-lookup"><span data-stu-id="9c3b1-144">Private Container Registry Password</span></span>

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

### <span data-ttu-id="9c3b1-145">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="9c3b1-145">-ContainerRegistryUrl</span></span>
<span data-ttu-id="9c3b1-146">Webb adress för privat behållarens register Server</span><span class="sxs-lookup"><span data-stu-id="9c3b1-146">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="9c3b1-147">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="9c3b1-147">-ContainerRegistryUser</span></span>
<span data-ttu-id="9c3b1-148">Användar namn för privat behållare</span><span class="sxs-lookup"><span data-stu-id="9c3b1-148">Private Container Registry Username</span></span>

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

### <span data-ttu-id="9c3b1-149">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="9c3b1-149">-DefaultDocuments</span></span>
<span data-ttu-id="9c3b1-150">Matris för standard dokument</span><span class="sxs-lookup"><span data-stu-id="9c3b1-150">Default Documents String Array</span></span>

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

### <span data-ttu-id="9c3b1-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c3b1-151">-DefaultProfile</span></span>
<span data-ttu-id="9c3b1-152">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9c3b1-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c3b1-153">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="9c3b1-153">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="9c3b1-154">Detaljerad fel loggning aktiverat boolesk</span><span class="sxs-lookup"><span data-stu-id="9c3b1-154">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="9c3b1-155">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="9c3b1-155">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="9c3b1-156">Aktiverar/inaktiverar kontinuerlig distribution av behållare webhook</span><span class="sxs-lookup"><span data-stu-id="9c3b1-156">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="9c3b1-157">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="9c3b1-157">-FtpsState</span></span>
<span data-ttu-id="9c3b1-158">Ange FTPS tillstånds värde för ett program.</span><span class="sxs-lookup"><span data-stu-id="9c3b1-158">Set the Ftps state value for an app.</span></span> <span data-ttu-id="9c3b1-159">Tillåtna värden [AllAllowed | Disabled | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="9c3b1-159">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="9c3b1-160">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="9c3b1-160">-HandlerMappings</span></span>
<span data-ttu-id="9c3b1-161">Hanterar mappningar IList</span><span class="sxs-lookup"><span data-stu-id="9c3b1-161">Handler Mappings IList</span></span>

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

### <span data-ttu-id="9c3b1-162">-Värdnamn</span><span class="sxs-lookup"><span data-stu-id="9c3b1-162">-HostNames</span></span>
<span data-ttu-id="9c3b1-163">Matris för WebApp-värdnamn</span><span class="sxs-lookup"><span data-stu-id="9c3b1-163">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="9c3b1-164">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="9c3b1-164">-HttpLoggingEnabled</span></span>
<span data-ttu-id="9c3b1-165">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="9c3b1-165">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="9c3b1-166">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="9c3b1-166">-HttpsOnly</span></span>
<span data-ttu-id="9c3b1-167">Aktivera/inaktivera omdirigering av all trafik till HTTPS på en befintlig Azure webapp eller functionapp</span><span class="sxs-lookup"><span data-stu-id="9c3b1-167">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="9c3b1-168">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="9c3b1-168">-ManagedPipelineMode</span></span>
<span data-ttu-id="9c3b1-169">Namn på hanterat pipeline-läge</span><span class="sxs-lookup"><span data-stu-id="9c3b1-169">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="9c3b1-170">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="9c3b1-170">-MinTlsVersion</span></span>
<span data-ttu-id="9c3b1-171">Den minsta versionen av TLS som krävs för SSL-begäranden.</span><span class="sxs-lookup"><span data-stu-id="9c3b1-171">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="9c3b1-172">Tillåtna värden [1,0 | 1,1 | 1,2].</span><span class="sxs-lookup"><span data-stu-id="9c3b1-172">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="9c3b1-173">-Namn</span><span class="sxs-lookup"><span data-stu-id="9c3b1-173">-Name</span></span>
<span data-ttu-id="9c3b1-174">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="9c3b1-174">WebApp Name</span></span>

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

### <span data-ttu-id="9c3b1-175">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="9c3b1-175">-NetFrameworkVersion</span></span>
<span data-ttu-id="9c3b1-176">NET Framework-version</span><span class="sxs-lookup"><span data-stu-id="9c3b1-176">Net Framework Version</span></span>

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

### <span data-ttu-id="9c3b1-177">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="9c3b1-177">-NumberOfWorkers</span></span>
<span data-ttu-id="9c3b1-178">Antalet arbetare som ska tilldelas</span><span class="sxs-lookup"><span data-stu-id="9c3b1-178">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="9c3b1-179">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="9c3b1-179">-PhpVersion</span></span>
<span data-ttu-id="9c3b1-180">Php-version</span><span class="sxs-lookup"><span data-stu-id="9c3b1-180">Php Version</span></span>

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

### <span data-ttu-id="9c3b1-181">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="9c3b1-181">-RequestTracingEnabled</span></span>
<span data-ttu-id="9c3b1-182">Begäran om spårning aktive rad</span><span class="sxs-lookup"><span data-stu-id="9c3b1-182">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="9c3b1-183">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c3b1-183">-ResourceGroupName</span></span>
<span data-ttu-id="9c3b1-184">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="9c3b1-184">Resource Group Name</span></span>

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

### <span data-ttu-id="9c3b1-185">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="9c3b1-185">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="9c3b1-186">Använda 32-bitars boolesk arbets process</span><span class="sxs-lookup"><span data-stu-id="9c3b1-186">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="9c3b1-187">-WebApp</span><span class="sxs-lookup"><span data-stu-id="9c3b1-187">-WebApp</span></span>
<span data-ttu-id="9c3b1-188">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="9c3b1-188">WebApp Object</span></span>

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

### <span data-ttu-id="9c3b1-189">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="9c3b1-189">-WebSocketsEnabled</span></span>
<span data-ttu-id="9c3b1-190">WebSocketsEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="9c3b1-190">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="9c3b1-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c3b1-191">CommonParameters</span></span>
<span data-ttu-id="9c3b1-192">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c3b1-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c3b1-193">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9c3b1-193">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c3b1-194">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9c3b1-194">INPUTS</span></span>

### <span data-ttu-id="9c3b1-195">System. Int32</span><span class="sxs-lookup"><span data-stu-id="9c3b1-195">System.Int32</span></span>

### <span data-ttu-id="9c3b1-196">System. String</span><span class="sxs-lookup"><span data-stu-id="9c3b1-196">System.String</span></span>

### <span data-ttu-id="9c3b1-197">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="9c3b1-197">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="9c3b1-198">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9c3b1-198">OUTPUTS</span></span>

### <span data-ttu-id="9c3b1-199">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="9c3b1-199">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="9c3b1-200">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9c3b1-200">NOTES</span></span>
<span data-ttu-id="9c3b1-201">Under angiven cmdlet kan du uppdatera Azure Web App till **DOTNETCORE**</span><span class="sxs-lookup"><span data-stu-id="9c3b1-201">Below provided cmdlet will help you to update Azure Web App to **DOTNETCORE**</span></span>

<span data-ttu-id="9c3b1-202">$PropertiesObject = @ {"CURRENT_STACK" = "dotnetcore"} New-AzResource-PropertyObject $PropertiesObject-ResourceGroupName "default-Web-West"-ResourceType Microsoft. Web/Sites/config-ResourceName "ContosoWebApp/metadata" – ApiVersion 2018-02-01-Force</span><span class="sxs-lookup"><span data-stu-id="9c3b1-202">$PropertiesObject = @{ "CURRENT_STACK" =  "dotnetcore" } New-AzResource -PropertyObject $PropertiesObject -ResourceGroupName "Default-Web-WestUS" -ResourceType Microsoft.Web/sites/config -ResourceName "ContosoWebApp/metadata" -ApiVersion 2018-02-01 -Force</span></span>

<span data-ttu-id="9c3b1-203">Ersätt värdena som standard-väst med ditt resurs grupp namn för webapp and ContosoWebApp med webapp-namnet.</span><span class="sxs-lookup"><span data-stu-id="9c3b1-203">Replace the values of Default-Web-WestUS with your resource group name of the webapp and ContosoWebApp with the webapp name.</span></span>
 
## <span data-ttu-id="9c3b1-204">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9c3b1-204">RELATED LINKS</span></span>

[<span data-ttu-id="9c3b1-205">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="9c3b1-205">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="9c3b1-206">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="9c3b1-206">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="9c3b1-207">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="9c3b1-207">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="9c3b1-208">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="9c3b1-208">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="9c3b1-209">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="9c3b1-209">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="9c3b1-210">Stopp-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="9c3b1-210">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)

[<span data-ttu-id="9c3b1-211">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="9c3b1-211">New-AzResource</span></span>](./New-AzResource.md)
