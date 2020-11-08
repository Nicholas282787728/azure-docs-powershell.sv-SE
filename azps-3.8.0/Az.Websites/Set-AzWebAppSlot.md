---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
ms.openlocfilehash: ed1e073757eb2fc1b63a6ffd799c55ad1ffaf748
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090327"
---
# <span data-ttu-id="1d4c6-101">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="1d4c6-101">Set-AzWebAppSlot</span></span>

## <span data-ttu-id="1d4c6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1d4c6-102">SYNOPSIS</span></span>
<span data-ttu-id="1d4c6-103">Ändrar en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="1d4c6-103">Modifies an Azure Web App slot.</span></span>

## <span data-ttu-id="1d4c6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1d4c6-104">SYNTAX</span></span>

### <span data-ttu-id="1d4c6-105">S</span><span class="sxs-lookup"><span data-stu-id="1d4c6-105">S1</span></span>
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

### <span data-ttu-id="1d4c6-106">S2</span><span class="sxs-lookup"><span data-stu-id="1d4c6-106">S2</span></span>
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

## <span data-ttu-id="1d4c6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1d4c6-107">DESCRIPTION</span></span>
<span data-ttu-id="1d4c6-108">Cmdleten **set-AzWebApp** anger en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="1d4c6-108">The **Set-AzWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="1d4c6-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1d4c6-109">EXAMPLES</span></span>

### <span data-ttu-id="1d4c6-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1d4c6-110">Example 1</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="1d4c6-111">Det här kommandot ändrar det AppService-abonnemang som är associerat med Slot001, på webapp-ContosoWebApp som är kopplad till resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="1d4c6-111">This command changes the appservice plan associated with the Slot001, on the Webapp ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="1d4c6-112">Använd länken för att lära dig mer om hur du ändrar AppService plan och vilka villkor som är associerade med den.</span><span class="sxs-lookup"><span data-stu-id="1d4c6-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="1d4c6-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="1d4c6-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="1d4c6-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="1d4c6-114">Example 2</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="1d4c6-115">Det här kommandot anger HttpLoggingEnabled till sant för fack Slot001 som hör till Web App-ContosoWebApp som är kopplad till resurs gruppens standard-väst</span><span class="sxs-lookup"><span data-stu-id="1d4c6-115">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="1d4c6-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1d4c6-116">PARAMETERS</span></span>

### <span data-ttu-id="1d4c6-117">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="1d4c6-117">-AlwaysOn</span></span>
<span data-ttu-id="1d4c6-118">Se till att webb programmet läses in hela tiden, i stället är inaktiverat.</span><span class="sxs-lookup"><span data-stu-id="1d4c6-118">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="1d4c6-119">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="1d4c6-119">-AppServicePlan</span></span>
<span data-ttu-id="1d4c6-120">Namn på App Service-abonnemang</span><span class="sxs-lookup"><span data-stu-id="1d4c6-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="1d4c6-121">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="1d4c6-121">-AppSettings</span></span>
<span data-ttu-id="1d4c6-122">App Settings-hash.</span><span class="sxs-lookup"><span data-stu-id="1d4c6-122">App Settings HashTable.</span></span> <span data-ttu-id="1d4c6-123">Befintliga program inställningar ersätts och tar bort alla inställningar som inte tillhandahålls.</span><span class="sxs-lookup"><span data-stu-id="1d4c6-123">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="1d4c6-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1d4c6-124">-AsJob</span></span>
<span data-ttu-id="1d4c6-125">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="1d4c6-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1d4c6-126">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="1d4c6-126">-AssignIdentity</span></span>
<span data-ttu-id="1d4c6-127">Aktivera/inaktivera MSI på en befintlig plats [för hands version]</span><span class="sxs-lookup"><span data-stu-id="1d4c6-127">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="1d4c6-128">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="1d4c6-128">-AutoSwapSlotName</span></span>
<span data-ttu-id="1d4c6-129">Mål plats namn för automatisk växling</span><span class="sxs-lookup"><span data-stu-id="1d4c6-129">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="1d4c6-130">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="1d4c6-130">-AzureStoragePath</span></span>
<span data-ttu-id="1d4c6-131">Azure-lagring för montering i en Web App för container.</span><span class="sxs-lookup"><span data-stu-id="1d4c6-131">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="1d4c6-132">Använda New-AzureRmWebAppAzureStoragePath för att skapa den</span><span class="sxs-lookup"><span data-stu-id="1d4c6-132">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="1d4c6-133">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="1d4c6-133">-ConnectionStrings</span></span>
<span data-ttu-id="1d4c6-134">Anslutnings strängar-hash</span><span class="sxs-lookup"><span data-stu-id="1d4c6-134">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="1d4c6-135">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="1d4c6-135">-ContainerImageName</span></span>
<span data-ttu-id="1d4c6-136">Bild namn för behållare</span><span class="sxs-lookup"><span data-stu-id="1d4c6-136">Container Image Name</span></span>

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

### <span data-ttu-id="1d4c6-137">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="1d4c6-137">-ContainerRegistryPassword</span></span>
<span data-ttu-id="1d4c6-138">Lösen ord för privat behållare</span><span class="sxs-lookup"><span data-stu-id="1d4c6-138">Private Container Registry Password</span></span>

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

### <span data-ttu-id="1d4c6-139">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="1d4c6-139">-ContainerRegistryUrl</span></span>
<span data-ttu-id="1d4c6-140">Webb adress för privat behållarens register Server</span><span class="sxs-lookup"><span data-stu-id="1d4c6-140">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="1d4c6-141">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="1d4c6-141">-ContainerRegistryUser</span></span>
<span data-ttu-id="1d4c6-142">Användar namn för privat behållare</span><span class="sxs-lookup"><span data-stu-id="1d4c6-142">Private Container Registry Username</span></span>

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

### <span data-ttu-id="1d4c6-143">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="1d4c6-143">-DefaultDocuments</span></span>
<span data-ttu-id="1d4c6-144">Matris för standard dokument</span><span class="sxs-lookup"><span data-stu-id="1d4c6-144">Default Documents String Array</span></span>

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

### <span data-ttu-id="1d4c6-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d4c6-145">-DefaultProfile</span></span>
<span data-ttu-id="1d4c6-146">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1d4c6-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d4c6-147">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="1d4c6-147">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="1d4c6-148">Detaljerad fel loggning aktiverat boolesk</span><span class="sxs-lookup"><span data-stu-id="1d4c6-148">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="1d4c6-149">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="1d4c6-149">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="1d4c6-150">Aktiverar/inaktiverar kontinuerlig distribution av behållare webhook</span><span class="sxs-lookup"><span data-stu-id="1d4c6-150">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="1d4c6-151">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="1d4c6-151">-FtpsState</span></span>
<span data-ttu-id="1d4c6-152">Ange FTPS tillstånds värde för ett program.</span><span class="sxs-lookup"><span data-stu-id="1d4c6-152">Set the Ftps state value for an app.</span></span> <span data-ttu-id="1d4c6-153">Tillåtna värden [AllAllowed | Disabled | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="1d4c6-153">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="1d4c6-154">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="1d4c6-154">-HandlerMappings</span></span>
<span data-ttu-id="1d4c6-155">Hanterar mappningar IList</span><span class="sxs-lookup"><span data-stu-id="1d4c6-155">Handler Mappings IList</span></span>

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

### <span data-ttu-id="1d4c6-156">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="1d4c6-156">-HttpLoggingEnabled</span></span>
<span data-ttu-id="1d4c6-157">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="1d4c6-157">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="1d4c6-158">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="1d4c6-158">-HttpsOnly</span></span>
<span data-ttu-id="1d4c6-159">Aktivera/inaktivera all trafik till HTTPS på en befintlig plats</span><span class="sxs-lookup"><span data-stu-id="1d4c6-159">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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

### <span data-ttu-id="1d4c6-160">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="1d4c6-160">-ManagedPipelineMode</span></span>
<span data-ttu-id="1d4c6-161">Namn på hanterat pipeline-läge</span><span class="sxs-lookup"><span data-stu-id="1d4c6-161">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="1d4c6-162">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="1d4c6-162">-MinTlsVersion</span></span>
<span data-ttu-id="1d4c6-163">Den minsta versionen av TLS som krävs för SSL-begäranden.</span><span class="sxs-lookup"><span data-stu-id="1d4c6-163">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="1d4c6-164">Tillåtna värden [1,0 | 1,1 | 1,2].</span><span class="sxs-lookup"><span data-stu-id="1d4c6-164">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="1d4c6-165">-Namn</span><span class="sxs-lookup"><span data-stu-id="1d4c6-165">-Name</span></span>
<span data-ttu-id="1d4c6-166">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="1d4c6-166">WebApp Name</span></span>

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

### <span data-ttu-id="1d4c6-167">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="1d4c6-167">-NetFrameworkVersion</span></span>
<span data-ttu-id="1d4c6-168">NET Framework-version</span><span class="sxs-lookup"><span data-stu-id="1d4c6-168">Net Framework Version</span></span>

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

### <span data-ttu-id="1d4c6-169">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="1d4c6-169">-NumberOfWorkers</span></span>
<span data-ttu-id="1d4c6-170">Antalet arbetare som ska tilldelas</span><span class="sxs-lookup"><span data-stu-id="1d4c6-170">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="1d4c6-171">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="1d4c6-171">-PhpVersion</span></span>
<span data-ttu-id="1d4c6-172">Php-version</span><span class="sxs-lookup"><span data-stu-id="1d4c6-172">Php Version</span></span>

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

### <span data-ttu-id="1d4c6-173">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="1d4c6-173">-RequestTracingEnabled</span></span>
<span data-ttu-id="1d4c6-174">Begäran om spårning aktiverat boolesk</span><span class="sxs-lookup"><span data-stu-id="1d4c6-174">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="1d4c6-175">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d4c6-175">-ResourceGroupName</span></span>
<span data-ttu-id="1d4c6-176">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="1d4c6-176">Resource Group Name</span></span>

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

### <span data-ttu-id="1d4c6-177">-Plats</span><span class="sxs-lookup"><span data-stu-id="1d4c6-177">-Slot</span></span>
<span data-ttu-id="1d4c6-178">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="1d4c6-178">WebApp Slot Name</span></span>

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

### <span data-ttu-id="1d4c6-179">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="1d4c6-179">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="1d4c6-180">Använda 32-bitars boolesk arbets process</span><span class="sxs-lookup"><span data-stu-id="1d4c6-180">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="1d4c6-181">-WebApp</span><span class="sxs-lookup"><span data-stu-id="1d4c6-181">-WebApp</span></span>
<span data-ttu-id="1d4c6-182">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="1d4c6-182">WebApp Object</span></span>

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

### <span data-ttu-id="1d4c6-183">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="1d4c6-183">-WebSocketsEnabled</span></span>
<span data-ttu-id="1d4c6-184">Boolesk aktiverat Boolean</span><span class="sxs-lookup"><span data-stu-id="1d4c6-184">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="1d4c6-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d4c6-185">CommonParameters</span></span>
<span data-ttu-id="1d4c6-186">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d4c6-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d4c6-187">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1d4c6-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d4c6-188">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1d4c6-188">INPUTS</span></span>

### <span data-ttu-id="1d4c6-189">System. Int32</span><span class="sxs-lookup"><span data-stu-id="1d4c6-189">System.Int32</span></span>

### <span data-ttu-id="1d4c6-190">System. String</span><span class="sxs-lookup"><span data-stu-id="1d4c6-190">System.String</span></span>

### <span data-ttu-id="1d4c6-191">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="1d4c6-191">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="1d4c6-192">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1d4c6-192">OUTPUTS</span></span>

### <span data-ttu-id="1d4c6-193">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="1d4c6-193">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="1d4c6-194">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1d4c6-194">NOTES</span></span>

## <span data-ttu-id="1d4c6-195">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1d4c6-195">RELATED LINKS</span></span>

[<span data-ttu-id="1d4c6-196">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="1d4c6-196">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="1d4c6-197">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="1d4c6-197">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="1d4c6-198">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="1d4c6-198">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="1d4c6-199">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="1d4c6-199">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="1d4c6-200">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="1d4c6-200">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="1d4c6-201">Stopp-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="1d4c6-201">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="1d4c6-202">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="1d4c6-202">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)
