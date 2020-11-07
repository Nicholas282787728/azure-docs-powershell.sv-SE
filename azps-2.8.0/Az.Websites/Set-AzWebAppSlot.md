---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
ms.openlocfilehash: 2dc2356557a56ced2c0c09b70a1f6c2787438034
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93921209"
---
# <span data-ttu-id="53bd0-101">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="53bd0-101">Set-AzWebAppSlot</span></span>

## <span data-ttu-id="53bd0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="53bd0-102">SYNOPSIS</span></span>
<span data-ttu-id="53bd0-103">Ändrar en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="53bd0-103">Modifies an Azure Web App slot.</span></span>

## <span data-ttu-id="53bd0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="53bd0-104">SYNTAX</span></span>

### <span data-ttu-id="53bd0-105">S</span><span class="sxs-lookup"><span data-stu-id="53bd0-105">S1</span></span>
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
 [-AzureStoragePath <WebAppAzureStoragePath[]>] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53bd0-106">S2</span><span class="sxs-lookup"><span data-stu-id="53bd0-106">S2</span></span>
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

## <span data-ttu-id="53bd0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="53bd0-107">DESCRIPTION</span></span>
<span data-ttu-id="53bd0-108">Cmdleten **set-AzWebApp** anger en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="53bd0-108">The **Set-AzWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="53bd0-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="53bd0-109">EXAMPLES</span></span>

### <span data-ttu-id="53bd0-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="53bd0-110">Example 1</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="53bd0-111">Det här kommandot ändrar det AppService-abonnemang som är associerat med Slot001, på webapp-ContosoWebApp som är kopplad till resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="53bd0-111">This command changes the appservice plan associated with the Slot001, on the Webapp ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="53bd0-112">Använd länken för att lära dig mer om hur du ändrar AppService plan och vilka villkor som är associerade med den.</span><span class="sxs-lookup"><span data-stu-id="53bd0-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="53bd0-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="53bd0-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="53bd0-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="53bd0-114">Example 2</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="53bd0-115">Det här kommandot anger HttpLoggingEnabled till sant för fack Slot001 som hör till Web App-ContosoWebApp som är kopplad till resurs gruppens standard-väst</span><span class="sxs-lookup"><span data-stu-id="53bd0-115">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="53bd0-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="53bd0-116">PARAMETERS</span></span>

### <span data-ttu-id="53bd0-117">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="53bd0-117">-AppServicePlan</span></span>
<span data-ttu-id="53bd0-118">Namn på App Service-abonnemang</span><span class="sxs-lookup"><span data-stu-id="53bd0-118">App Service Plan Name</span></span>

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

### <span data-ttu-id="53bd0-119">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="53bd0-119">-AppSettings</span></span>
<span data-ttu-id="53bd0-120">App Settings-hash.</span><span class="sxs-lookup"><span data-stu-id="53bd0-120">App Settings HashTable.</span></span> <span data-ttu-id="53bd0-121">Befintliga program inställningar ersätts och tar bort alla inställningar som inte tillhandahålls.</span><span class="sxs-lookup"><span data-stu-id="53bd0-121">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="53bd0-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="53bd0-122">-AsJob</span></span>
<span data-ttu-id="53bd0-123">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="53bd0-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="53bd0-124">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="53bd0-124">-AssignIdentity</span></span>
<span data-ttu-id="53bd0-125">Aktivera/inaktivera MSI på en befintlig plats [för hands version]</span><span class="sxs-lookup"><span data-stu-id="53bd0-125">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="53bd0-126">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="53bd0-126">-AutoSwapSlotName</span></span>
<span data-ttu-id="53bd0-127">Mål plats namn för automatisk växling</span><span class="sxs-lookup"><span data-stu-id="53bd0-127">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="53bd0-128">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="53bd0-128">-AzureStoragePath</span></span>
<span data-ttu-id="53bd0-129">Azure-lagring för montering i en Web App för container.</span><span class="sxs-lookup"><span data-stu-id="53bd0-129">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="53bd0-130">Använda New-AzureRmWebAppAzureStoragePath för att skapa den</span><span class="sxs-lookup"><span data-stu-id="53bd0-130">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="53bd0-131">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="53bd0-131">-ConnectionStrings</span></span>
<span data-ttu-id="53bd0-132">Anslutnings strängar-hash</span><span class="sxs-lookup"><span data-stu-id="53bd0-132">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="53bd0-133">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="53bd0-133">-ContainerImageName</span></span>
<span data-ttu-id="53bd0-134">Bild namn för behållare</span><span class="sxs-lookup"><span data-stu-id="53bd0-134">Container Image Name</span></span>

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

### <span data-ttu-id="53bd0-135">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="53bd0-135">-ContainerRegistryPassword</span></span>
<span data-ttu-id="53bd0-136">Lösen ord för privat behållare</span><span class="sxs-lookup"><span data-stu-id="53bd0-136">Private Container Registry Password</span></span>

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

### <span data-ttu-id="53bd0-137">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="53bd0-137">-ContainerRegistryUrl</span></span>
<span data-ttu-id="53bd0-138">Webb adress för privat behållarens register Server</span><span class="sxs-lookup"><span data-stu-id="53bd0-138">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="53bd0-139">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="53bd0-139">-ContainerRegistryUser</span></span>
<span data-ttu-id="53bd0-140">Användar namn för privat behållare</span><span class="sxs-lookup"><span data-stu-id="53bd0-140">Private Container Registry Username</span></span>

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

### <span data-ttu-id="53bd0-141">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="53bd0-141">-DefaultDocuments</span></span>
<span data-ttu-id="53bd0-142">Matris för standard dokument</span><span class="sxs-lookup"><span data-stu-id="53bd0-142">Default Documents String Array</span></span>

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

### <span data-ttu-id="53bd0-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53bd0-143">-DefaultProfile</span></span>
<span data-ttu-id="53bd0-144">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="53bd0-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53bd0-145">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="53bd0-145">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="53bd0-146">Detaljerad fel loggning aktiverat boolesk</span><span class="sxs-lookup"><span data-stu-id="53bd0-146">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="53bd0-147">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="53bd0-147">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="53bd0-148">Aktiverar/inaktiverar kontinuerlig distribution av behållare webhook</span><span class="sxs-lookup"><span data-stu-id="53bd0-148">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="53bd0-149">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="53bd0-149">-HandlerMappings</span></span>
<span data-ttu-id="53bd0-150">Hanterar mappningar IList</span><span class="sxs-lookup"><span data-stu-id="53bd0-150">Handler Mappings IList</span></span>

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

### <span data-ttu-id="53bd0-151">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="53bd0-151">-HttpLoggingEnabled</span></span>
<span data-ttu-id="53bd0-152">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="53bd0-152">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="53bd0-153">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="53bd0-153">-HttpsOnly</span></span>
<span data-ttu-id="53bd0-154">Aktivera/inaktivera all trafik till HTTPS på en befintlig plats</span><span class="sxs-lookup"><span data-stu-id="53bd0-154">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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

### <span data-ttu-id="53bd0-155">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="53bd0-155">-ManagedPipelineMode</span></span>
<span data-ttu-id="53bd0-156">Namn på hanterat pipeline-läge</span><span class="sxs-lookup"><span data-stu-id="53bd0-156">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="53bd0-157">-Namn</span><span class="sxs-lookup"><span data-stu-id="53bd0-157">-Name</span></span>
<span data-ttu-id="53bd0-158">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="53bd0-158">WebApp Name</span></span>

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

### <span data-ttu-id="53bd0-159">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="53bd0-159">-NetFrameworkVersion</span></span>
<span data-ttu-id="53bd0-160">NET Framework-version</span><span class="sxs-lookup"><span data-stu-id="53bd0-160">Net Framework Version</span></span>

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

### <span data-ttu-id="53bd0-161">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="53bd0-161">-NumberOfWorkers</span></span>
<span data-ttu-id="53bd0-162">Antalet arbetare som ska tilldelas</span><span class="sxs-lookup"><span data-stu-id="53bd0-162">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="53bd0-163">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="53bd0-163">-PhpVersion</span></span>
<span data-ttu-id="53bd0-164">Php-version</span><span class="sxs-lookup"><span data-stu-id="53bd0-164">Php Version</span></span>

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

### <span data-ttu-id="53bd0-165">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="53bd0-165">-RequestTracingEnabled</span></span>
<span data-ttu-id="53bd0-166">Begäran om spårning aktiverat boolesk</span><span class="sxs-lookup"><span data-stu-id="53bd0-166">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="53bd0-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53bd0-167">-ResourceGroupName</span></span>
<span data-ttu-id="53bd0-168">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="53bd0-168">Resource Group Name</span></span>

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

### <span data-ttu-id="53bd0-169">-Plats</span><span class="sxs-lookup"><span data-stu-id="53bd0-169">-Slot</span></span>
<span data-ttu-id="53bd0-170">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="53bd0-170">WebApp Slot Name</span></span>

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

### <span data-ttu-id="53bd0-171">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="53bd0-171">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="53bd0-172">Använda 32-bitars boolesk arbets process</span><span class="sxs-lookup"><span data-stu-id="53bd0-172">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="53bd0-173">-WebApp</span><span class="sxs-lookup"><span data-stu-id="53bd0-173">-WebApp</span></span>
<span data-ttu-id="53bd0-174">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="53bd0-174">WebApp Object</span></span>

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

### <span data-ttu-id="53bd0-175">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="53bd0-175">-WebSocketsEnabled</span></span>
<span data-ttu-id="53bd0-176">Boolesk aktiverat Boolean</span><span class="sxs-lookup"><span data-stu-id="53bd0-176">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="53bd0-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53bd0-177">CommonParameters</span></span>
<span data-ttu-id="53bd0-178">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53bd0-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53bd0-179">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53bd0-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53bd0-180">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="53bd0-180">INPUTS</span></span>

### <span data-ttu-id="53bd0-181">System. Int32</span><span class="sxs-lookup"><span data-stu-id="53bd0-181">System.Int32</span></span>

### <span data-ttu-id="53bd0-182">System. String</span><span class="sxs-lookup"><span data-stu-id="53bd0-182">System.String</span></span>

### <span data-ttu-id="53bd0-183">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="53bd0-183">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="53bd0-184">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="53bd0-184">OUTPUTS</span></span>

### <span data-ttu-id="53bd0-185">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="53bd0-185">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="53bd0-186">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="53bd0-186">NOTES</span></span>

## <span data-ttu-id="53bd0-187">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="53bd0-187">RELATED LINKS</span></span>

[<span data-ttu-id="53bd0-188">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="53bd0-188">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="53bd0-189">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="53bd0-189">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="53bd0-190">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="53bd0-190">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="53bd0-191">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="53bd0-191">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="53bd0-192">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="53bd0-192">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="53bd0-193">Stopp-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="53bd0-193">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="53bd0-194">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="53bd0-194">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)
