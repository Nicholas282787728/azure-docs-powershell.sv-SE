---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
ms.openlocfilehash: d0bca8fadf9179990eb5901e67ee07a3532a39cb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746019"
---
# <span data-ttu-id="d3099-101">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d3099-101">Set-AzWebAppSlot</span></span>

## <span data-ttu-id="d3099-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d3099-102">SYNOPSIS</span></span>
<span data-ttu-id="d3099-103">Ändrar en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="d3099-103">Modifies an Azure Web App slot.</span></span>

## <span data-ttu-id="d3099-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d3099-104">SYNTAX</span></span>

### <span data-ttu-id="d3099-105">S</span><span class="sxs-lookup"><span data-stu-id="d3099-105">S1</span></span>
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

### <span data-ttu-id="d3099-106">S2</span><span class="sxs-lookup"><span data-stu-id="d3099-106">S2</span></span>
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

## <span data-ttu-id="d3099-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d3099-107">DESCRIPTION</span></span>
<span data-ttu-id="d3099-108">Cmdleten **set-AzWebApp** anger en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="d3099-108">The **Set-AzWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="d3099-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d3099-109">EXAMPLES</span></span>

### <span data-ttu-id="d3099-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d3099-110">Example 1</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="d3099-111">Det här kommandot ändrar det AppService-abonnemang som är associerat med Slot001, på webapp-ContosoWebApp som är kopplad till resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="d3099-111">This command changes the appservice plan associated with the Slot001, on the Webapp ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="d3099-112">Använd länken för att rensa mer om hur du ändrar AppService plan och vilka villkor som är associerade med den.</span><span class="sxs-lookup"><span data-stu-id="d3099-112">Use the link to learm more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="d3099-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="d3099-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="d3099-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="d3099-114">Example 2</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="d3099-115">Det här kommandot anger HttpLoggingEnabled till sant för fack Slot001 som hör till Web App-ContosoWebApp som är kopplad till resurs gruppens standard-väst</span><span class="sxs-lookup"><span data-stu-id="d3099-115">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="d3099-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d3099-116">PARAMETERS</span></span>

### <span data-ttu-id="d3099-117">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d3099-117">-AppServicePlan</span></span>
<span data-ttu-id="d3099-118">Namn på App Service-abonnemang</span><span class="sxs-lookup"><span data-stu-id="d3099-118">App Service Plan Name</span></span>

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

### <span data-ttu-id="d3099-119">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="d3099-119">-AppSettings</span></span>
<span data-ttu-id="d3099-120">App Settings-hash</span><span class="sxs-lookup"><span data-stu-id="d3099-120">App Settings HashTable</span></span>

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

### <span data-ttu-id="d3099-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d3099-121">-AsJob</span></span>
<span data-ttu-id="d3099-122">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="d3099-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d3099-123">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="d3099-123">-AssignIdentity</span></span>
<span data-ttu-id="d3099-124">Aktivera/inaktivera MSI på en befintlig plats [för hands version]</span><span class="sxs-lookup"><span data-stu-id="d3099-124">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="d3099-125">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="d3099-125">-AutoSwapSlotName</span></span>
<span data-ttu-id="d3099-126">Mål plats namn för automatisk växling</span><span class="sxs-lookup"><span data-stu-id="d3099-126">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="d3099-127">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="d3099-127">-AzureStoragePath</span></span>
<span data-ttu-id="d3099-128">Azure-lagring för montering i en Web App för container.</span><span class="sxs-lookup"><span data-stu-id="d3099-128">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="d3099-129">Använda New-AzureRmWebAppAzureStoragePath för att skapa den</span><span class="sxs-lookup"><span data-stu-id="d3099-129">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="d3099-130">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="d3099-130">-ConnectionStrings</span></span>
<span data-ttu-id="d3099-131">Anslutnings strängar-hash</span><span class="sxs-lookup"><span data-stu-id="d3099-131">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="d3099-132">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="d3099-132">-ContainerImageName</span></span>
<span data-ttu-id="d3099-133">Bild namn för behållare</span><span class="sxs-lookup"><span data-stu-id="d3099-133">Container Image Name</span></span>

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

### <span data-ttu-id="d3099-134">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="d3099-134">-ContainerRegistryPassword</span></span>
<span data-ttu-id="d3099-135">Lösen ord för privat behållare</span><span class="sxs-lookup"><span data-stu-id="d3099-135">Private Container Registry Password</span></span>

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

### <span data-ttu-id="d3099-136">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="d3099-136">-ContainerRegistryUrl</span></span>
<span data-ttu-id="d3099-137">Webb adress för privat behållarens register Server</span><span class="sxs-lookup"><span data-stu-id="d3099-137">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="d3099-138">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="d3099-138">-ContainerRegistryUser</span></span>
<span data-ttu-id="d3099-139">Användar namn för privat behållare</span><span class="sxs-lookup"><span data-stu-id="d3099-139">Private Container Registry Username</span></span>

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

### <span data-ttu-id="d3099-140">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="d3099-140">-DefaultDocuments</span></span>
<span data-ttu-id="d3099-141">Matris för standard dokument</span><span class="sxs-lookup"><span data-stu-id="d3099-141">Default Documents String Array</span></span>

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

### <span data-ttu-id="d3099-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3099-142">-DefaultProfile</span></span>
<span data-ttu-id="d3099-143">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d3099-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3099-144">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="d3099-144">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="d3099-145">Detaljerad fel loggning aktiverat boolesk</span><span class="sxs-lookup"><span data-stu-id="d3099-145">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="d3099-146">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="d3099-146">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="d3099-147">Aktiverar/inaktiverar kontinuerlig distribution av behållare webhook</span><span class="sxs-lookup"><span data-stu-id="d3099-147">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="d3099-148">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="d3099-148">-HandlerMappings</span></span>
<span data-ttu-id="d3099-149">Hanterar mappningar IList</span><span class="sxs-lookup"><span data-stu-id="d3099-149">Handler Mappings IList</span></span>

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

### <span data-ttu-id="d3099-150">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="d3099-150">-HttpLoggingEnabled</span></span>
<span data-ttu-id="d3099-151">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="d3099-151">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="d3099-152">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="d3099-152">-HttpsOnly</span></span>
<span data-ttu-id="d3099-153">Aktivera/inaktivera all trafik till HTTPS på en befintlig plats</span><span class="sxs-lookup"><span data-stu-id="d3099-153">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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

### <span data-ttu-id="d3099-154">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="d3099-154">-ManagedPipelineMode</span></span>
<span data-ttu-id="d3099-155">Namn på hanterat pipeline-läge</span><span class="sxs-lookup"><span data-stu-id="d3099-155">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="d3099-156">-Namn</span><span class="sxs-lookup"><span data-stu-id="d3099-156">-Name</span></span>
<span data-ttu-id="d3099-157">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="d3099-157">WebApp Name</span></span>

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

### <span data-ttu-id="d3099-158">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="d3099-158">-NetFrameworkVersion</span></span>
<span data-ttu-id="d3099-159">NET Framework-version</span><span class="sxs-lookup"><span data-stu-id="d3099-159">Net Framework Version</span></span>

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

### <span data-ttu-id="d3099-160">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="d3099-160">-NumberOfWorkers</span></span>
<span data-ttu-id="d3099-161">Antalet arbetare som ska tilldelas</span><span class="sxs-lookup"><span data-stu-id="d3099-161">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="d3099-162">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="d3099-162">-PhpVersion</span></span>
<span data-ttu-id="d3099-163">Php-version</span><span class="sxs-lookup"><span data-stu-id="d3099-163">Php Version</span></span>

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

### <span data-ttu-id="d3099-164">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="d3099-164">-RequestTracingEnabled</span></span>
<span data-ttu-id="d3099-165">Begäran om spårning aktiverat boolesk</span><span class="sxs-lookup"><span data-stu-id="d3099-165">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="d3099-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3099-166">-ResourceGroupName</span></span>
<span data-ttu-id="d3099-167">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="d3099-167">Resource Group Name</span></span>

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

### <span data-ttu-id="d3099-168">-Plats</span><span class="sxs-lookup"><span data-stu-id="d3099-168">-Slot</span></span>
<span data-ttu-id="d3099-169">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="d3099-169">WebApp Slot Name</span></span>

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

### <span data-ttu-id="d3099-170">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="d3099-170">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="d3099-171">Använda 32-bitars boolesk arbets process</span><span class="sxs-lookup"><span data-stu-id="d3099-171">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="d3099-172">-WebApp</span><span class="sxs-lookup"><span data-stu-id="d3099-172">-WebApp</span></span>
<span data-ttu-id="d3099-173">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="d3099-173">WebApp Object</span></span>

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

### <span data-ttu-id="d3099-174">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="d3099-174">-WebSocketsEnabled</span></span>
<span data-ttu-id="d3099-175">Boolesk aktiverat Boolean</span><span class="sxs-lookup"><span data-stu-id="d3099-175">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="d3099-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3099-176">CommonParameters</span></span>
<span data-ttu-id="d3099-177">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3099-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3099-178">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3099-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3099-179">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d3099-179">INPUTS</span></span>

### <span data-ttu-id="d3099-180">System. Int32</span><span class="sxs-lookup"><span data-stu-id="d3099-180">System.Int32</span></span>

### <span data-ttu-id="d3099-181">System. String</span><span class="sxs-lookup"><span data-stu-id="d3099-181">System.String</span></span>

### <span data-ttu-id="d3099-182">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="d3099-182">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="d3099-183">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d3099-183">OUTPUTS</span></span>

### <span data-ttu-id="d3099-184">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="d3099-184">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="d3099-185">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d3099-185">NOTES</span></span>

## <span data-ttu-id="d3099-186">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d3099-186">RELATED LINKS</span></span>

[<span data-ttu-id="d3099-187">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d3099-187">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="d3099-188">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d3099-188">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="d3099-189">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d3099-189">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="d3099-190">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d3099-190">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="d3099-191">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d3099-191">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="d3099-192">Stopp-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d3099-192">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="d3099-193">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d3099-193">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)
