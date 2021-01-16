---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
ms.openlocfilehash: 5f465f97ab5f5bec817619709359179acff38043
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522055"
---
# <span data-ttu-id="5bced-101">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5bced-101">Set-AzWebAppSlot</span></span>

## <span data-ttu-id="5bced-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5bced-102">SYNOPSIS</span></span>
<span data-ttu-id="5bced-103">Ändrar en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="5bced-103">Modifies an Azure Web App slot.</span></span>

## <span data-ttu-id="5bced-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5bced-104">SYNTAX</span></span>

### <span data-ttu-id="5bced-105">S</span><span class="sxs-lookup"><span data-stu-id="5bced-105">S1</span></span>
```
Set-AzWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-ContainerImageName <String>]
 [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>] [-ContainerRegistryPassword <SecureString>]
 [-EnableContainerContinuousDeployment <Boolean>] [-AsJob] [-AssignIdentity <Boolean>] [-HttpsOnly <Boolean>]
 [-AzureStoragePath <WebAppAzureStoragePath[]>] [-AlwaysOn <Boolean>] [-MinTlsVersion <String>]
 [-FtpsState <String>] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5bced-106">S2</span><span class="sxs-lookup"><span data-stu-id="5bced-106">S2</span></span>
```
Set-AzWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-AsJob] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5bced-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5bced-107">DESCRIPTION</span></span>
<span data-ttu-id="5bced-108">Cmdleten **set-AzWebApp** anger en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="5bced-108">The **Set-AzWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="5bced-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5bced-109">EXAMPLES</span></span>

### <span data-ttu-id="5bced-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5bced-110">Example 1</span></span>
```powershell
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="5bced-111">Det här kommandot ändrar det AppService-abonnemang som är associerat med Slot001, på webapp-ContosoWebApp som är kopplad till resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="5bced-111">This command changes the appservice plan associated with the Slot001, on the Webapp ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="5bced-112">Använd länken för att lära dig mer om hur du ändrar AppService plan och vilka villkor som är associerade med den.</span><span class="sxs-lookup"><span data-stu-id="5bced-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="5bced-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="5bced-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="5bced-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="5bced-114">Example 2</span></span>
```powershell
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="5bced-115">Det här kommandot anger HttpLoggingEnabled till sant för fack Slot001 som hör till Web App-ContosoWebApp som är kopplad till resurs gruppens standard-väst</span><span class="sxs-lookup"><span data-stu-id="5bced-115">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

### <span data-ttu-id="5bced-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="5bced-116">Example 3</span></span>

<span data-ttu-id="5bced-117">Ändrar en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="5bced-117">Modifies an Azure Web App slot.</span></span> <span data-ttu-id="5bced-118">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="5bced-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzWebAppSlot -AppSettings <Hashtable> -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS' -Slot 'Slot001'
```

## <span data-ttu-id="5bced-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5bced-119">PARAMETERS</span></span>

### <span data-ttu-id="5bced-120">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="5bced-120">-AlwaysOn</span></span>
<span data-ttu-id="5bced-121">Se till att webb programmet läses in hela tiden, i stället är inaktiverat.</span><span class="sxs-lookup"><span data-stu-id="5bced-121">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="5bced-122">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="5bced-122">-AppServicePlan</span></span>
<span data-ttu-id="5bced-123">Namn på App Service-abonnemang</span><span class="sxs-lookup"><span data-stu-id="5bced-123">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bced-124">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="5bced-124">-AppSettings</span></span>
<span data-ttu-id="5bced-125">App Settings-hash.</span><span class="sxs-lookup"><span data-stu-id="5bced-125">App Settings HashTable.</span></span> <span data-ttu-id="5bced-126">Befintliga program inställningar ersätts och tar bort alla inställningar som inte tillhandahålls.</span><span class="sxs-lookup"><span data-stu-id="5bced-126">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bced-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5bced-127">-AsJob</span></span>
<span data-ttu-id="5bced-128">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="5bced-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5bced-129">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="5bced-129">-AssignIdentity</span></span>
<span data-ttu-id="5bced-130">Aktivera/inaktivera MSI på en befintlig plats [för hands version]</span><span class="sxs-lookup"><span data-stu-id="5bced-130">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="5bced-131">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="5bced-131">-AutoSwapSlotName</span></span>
<span data-ttu-id="5bced-132">Mål plats namn för automatisk växling</span><span class="sxs-lookup"><span data-stu-id="5bced-132">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="5bced-133">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="5bced-133">-AzureStoragePath</span></span>
<span data-ttu-id="5bced-134">Azure-lagring för montering i en Web App för container.</span><span class="sxs-lookup"><span data-stu-id="5bced-134">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="5bced-135">Använda New-AzureRmWebAppAzureStoragePath för att skapa den</span><span class="sxs-lookup"><span data-stu-id="5bced-135">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="5bced-136">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="5bced-136">-ConnectionStrings</span></span>
<span data-ttu-id="5bced-137">Anslutnings strängar-hash</span><span class="sxs-lookup"><span data-stu-id="5bced-137">Connection Strings HashTable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bced-138">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="5bced-138">-ContainerImageName</span></span>
<span data-ttu-id="5bced-139">Bild namn för behållare</span><span class="sxs-lookup"><span data-stu-id="5bced-139">Container Image Name</span></span>

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

### <span data-ttu-id="5bced-140">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="5bced-140">-ContainerRegistryPassword</span></span>
<span data-ttu-id="5bced-141">Lösen ord för privat behållare</span><span class="sxs-lookup"><span data-stu-id="5bced-141">Private Container Registry Password</span></span>

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

### <span data-ttu-id="5bced-142">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="5bced-142">-ContainerRegistryUrl</span></span>
<span data-ttu-id="5bced-143">Webb adress för privat behållarens register Server</span><span class="sxs-lookup"><span data-stu-id="5bced-143">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="5bced-144">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="5bced-144">-ContainerRegistryUser</span></span>
<span data-ttu-id="5bced-145">Användar namn för privat behållare</span><span class="sxs-lookup"><span data-stu-id="5bced-145">Private Container Registry Username</span></span>

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

### <span data-ttu-id="5bced-146">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="5bced-146">-DefaultDocuments</span></span>
<span data-ttu-id="5bced-147">Matris för standard dokument</span><span class="sxs-lookup"><span data-stu-id="5bced-147">Default Documents String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bced-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bced-148">-DefaultProfile</span></span>
<span data-ttu-id="5bced-149">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5bced-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5bced-150">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="5bced-150">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="5bced-151">Detaljerad fel loggning aktiverat boolesk</span><span class="sxs-lookup"><span data-stu-id="5bced-151">Detailed Error Logging Enabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bced-152">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="5bced-152">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="5bced-153">Aktiverar/inaktiverar kontinuerlig distribution av behållare webhook</span><span class="sxs-lookup"><span data-stu-id="5bced-153">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="5bced-154">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="5bced-154">-FtpsState</span></span>
<span data-ttu-id="5bced-155">Ange FTPS tillstånds värde för ett program.</span><span class="sxs-lookup"><span data-stu-id="5bced-155">Set the Ftps state value for an app.</span></span> <span data-ttu-id="5bced-156">Tillåtna värden [AllAllowed | Disabled | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="5bced-156">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="5bced-157">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="5bced-157">-HandlerMappings</span></span>
<span data-ttu-id="5bced-158">Hanterar mappningar IList</span><span class="sxs-lookup"><span data-stu-id="5bced-158">Handler Mappings IList</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]
Parameter Sets: (All)
Aliases:

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bced-159">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="5bced-159">-HttpLoggingEnabled</span></span>
<span data-ttu-id="5bced-160">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="5bced-160">HttpLoggingEnabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bced-161">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="5bced-161">-HttpsOnly</span></span>
<span data-ttu-id="5bced-162">Aktivera/inaktivera all trafik till HTTPS på en befintlig plats</span><span class="sxs-lookup"><span data-stu-id="5bced-162">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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

### <span data-ttu-id="5bced-163">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="5bced-163">-ManagedPipelineMode</span></span>
<span data-ttu-id="5bced-164">Namn på hanterat pipeline-läge</span><span class="sxs-lookup"><span data-stu-id="5bced-164">Managed Pipeline Mode Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Classic, Integrated

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bced-165">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="5bced-165">-MinTlsVersion</span></span>
<span data-ttu-id="5bced-166">Den minsta versionen av TLS som krävs för SSL-begäranden.</span><span class="sxs-lookup"><span data-stu-id="5bced-166">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="5bced-167">Tillåtna värden [1,0 | 1,1 | 1,2].</span><span class="sxs-lookup"><span data-stu-id="5bced-167">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="5bced-168">-Namn</span><span class="sxs-lookup"><span data-stu-id="5bced-168">-Name</span></span>
<span data-ttu-id="5bced-169">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="5bced-169">WebApp Name</span></span>

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

### <span data-ttu-id="5bced-170">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="5bced-170">-NetFrameworkVersion</span></span>
<span data-ttu-id="5bced-171">NET Framework-version</span><span class="sxs-lookup"><span data-stu-id="5bced-171">Net Framework Version</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bced-172">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="5bced-172">-NumberOfWorkers</span></span>
<span data-ttu-id="5bced-173">Antalet arbetare som ska tilldelas</span><span class="sxs-lookup"><span data-stu-id="5bced-173">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="5bced-174">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="5bced-174">-PhpVersion</span></span>
<span data-ttu-id="5bced-175">Php-version</span><span class="sxs-lookup"><span data-stu-id="5bced-175">Php Version</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bced-176">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="5bced-176">-RequestTracingEnabled</span></span>
<span data-ttu-id="5bced-177">Begäran om spårning aktiverat boolesk</span><span class="sxs-lookup"><span data-stu-id="5bced-177">Request Tracing Enabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bced-178">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bced-178">-ResourceGroupName</span></span>
<span data-ttu-id="5bced-179">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="5bced-179">Resource Group Name</span></span>

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

### <span data-ttu-id="5bced-180">-Plats</span><span class="sxs-lookup"><span data-stu-id="5bced-180">-Slot</span></span>
<span data-ttu-id="5bced-181">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="5bced-181">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bced-182">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="5bced-182">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="5bced-183">Använda 32-bitars boolesk arbets process</span><span class="sxs-lookup"><span data-stu-id="5bced-183">Use 32-bit Worker Process Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 15
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bced-184">-WebApp</span><span class="sxs-lookup"><span data-stu-id="5bced-184">-WebApp</span></span>
<span data-ttu-id="5bced-185">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="5bced-185">WebApp Object</span></span>

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

### <span data-ttu-id="5bced-186">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="5bced-186">-WebSocketsEnabled</span></span>
<span data-ttu-id="5bced-187">Boolesk aktiverat Boolean</span><span class="sxs-lookup"><span data-stu-id="5bced-187">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="5bced-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bced-188">CommonParameters</span></span>
<span data-ttu-id="5bced-189">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bced-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bced-190">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5bced-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bced-191">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5bced-191">INPUTS</span></span>

### <span data-ttu-id="5bced-192">System. Int32</span><span class="sxs-lookup"><span data-stu-id="5bced-192">System.Int32</span></span>

### <span data-ttu-id="5bced-193">System. String</span><span class="sxs-lookup"><span data-stu-id="5bced-193">System.String</span></span>

### <span data-ttu-id="5bced-194">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="5bced-194">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="5bced-195">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5bced-195">OUTPUTS</span></span>

### <span data-ttu-id="5bced-196">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="5bced-196">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="5bced-197">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5bced-197">NOTES</span></span>

## <span data-ttu-id="5bced-198">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5bced-198">RELATED LINKS</span></span>

[<span data-ttu-id="5bced-199">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5bced-199">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="5bced-200">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5bced-200">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="5bced-201">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5bced-201">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="5bced-202">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5bced-202">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="5bced-203">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5bced-203">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="5bced-204">Stopp-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5bced-204">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="5bced-205">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="5bced-205">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)
