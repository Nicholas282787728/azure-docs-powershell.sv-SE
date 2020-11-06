---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlot.md
ms.openlocfilehash: 4ba94f0f7633feefc32c0b32d820e8bee9b6d1b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577719"
---
# <span data-ttu-id="1461d-101">Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="1461d-101">Set-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="1461d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1461d-102">SYNOPSIS</span></span>
<span data-ttu-id="1461d-103">Ändrar en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="1461d-103">Modifies an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1461d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1461d-104">SYNTAX</span></span>

### <span data-ttu-id="1461d-105">S</span><span class="sxs-lookup"><span data-stu-id="1461d-105">S1</span></span>
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-ContainerImageName <String>]
 [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>] [-ContainerRegistryPassword <SecureString>]
 [-EnableContainerContinuousDeployment <Boolean>] [-AsJob] [-AssignIdentity <Boolean>] [-HttpsOnly <Boolean>]
 [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1461d-106">S2</span><span class="sxs-lookup"><span data-stu-id="1461d-106">S2</span></span>
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-AsJob] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1461d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1461d-107">DESCRIPTION</span></span>
<span data-ttu-id="1461d-108">Cmdleten **set-AzureRmWebApp** anger en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="1461d-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="1461d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1461d-109">EXAMPLES</span></span>

### <span data-ttu-id="1461d-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1461d-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="1461d-111">Det här kommandot anger HttpLoggingEnabled till sant för fack Slot001 som hör till Web App-ContosoWebApp som är kopplad till resurs gruppens standard-väst</span><span class="sxs-lookup"><span data-stu-id="1461d-111">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="1461d-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1461d-112">PARAMETERS</span></span>

### <span data-ttu-id="1461d-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="1461d-113">-AppServicePlan</span></span>
<span data-ttu-id="1461d-114">Namn på App Service-abonnemang</span><span class="sxs-lookup"><span data-stu-id="1461d-114">App Service Plan Name</span></span>

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

### <span data-ttu-id="1461d-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="1461d-115">-AppSettings</span></span>
<span data-ttu-id="1461d-116">App Settings-hash</span><span class="sxs-lookup"><span data-stu-id="1461d-116">App Settings HashTable</span></span>

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

### <span data-ttu-id="1461d-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1461d-117">-AsJob</span></span>
<span data-ttu-id="1461d-118">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="1461d-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1461d-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="1461d-119">-AssignIdentity</span></span>
<span data-ttu-id="1461d-120">Aktivera/inaktivera MSI på en befintlig plats [för hands version]</span><span class="sxs-lookup"><span data-stu-id="1461d-120">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="1461d-121">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="1461d-121">-AutoSwapSlotName</span></span>
<span data-ttu-id="1461d-122">Mål plats namn för automatisk växling</span><span class="sxs-lookup"><span data-stu-id="1461d-122">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="1461d-123">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="1461d-123">-ConnectionStrings</span></span>
<span data-ttu-id="1461d-124">Anslutnings strängar-hash</span><span class="sxs-lookup"><span data-stu-id="1461d-124">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="1461d-125">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="1461d-125">-ContainerImageName</span></span>
<span data-ttu-id="1461d-126">Bild namn för behållare</span><span class="sxs-lookup"><span data-stu-id="1461d-126">Container Image Name</span></span>

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

### <span data-ttu-id="1461d-127">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="1461d-127">-ContainerRegistryPassword</span></span>
<span data-ttu-id="1461d-128">Lösen ord för privat behållare</span><span class="sxs-lookup"><span data-stu-id="1461d-128">Private Container Registry Password</span></span>

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

### <span data-ttu-id="1461d-129">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="1461d-129">-ContainerRegistryUrl</span></span>
<span data-ttu-id="1461d-130">Webb adress för privat behållarens register Server</span><span class="sxs-lookup"><span data-stu-id="1461d-130">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="1461d-131">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="1461d-131">-ContainerRegistryUser</span></span>
<span data-ttu-id="1461d-132">Användar namn för privat behållare</span><span class="sxs-lookup"><span data-stu-id="1461d-132">Private Container Registry Username</span></span>

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

### <span data-ttu-id="1461d-133">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="1461d-133">-DefaultDocuments</span></span>
<span data-ttu-id="1461d-134">Matris för standard dokument</span><span class="sxs-lookup"><span data-stu-id="1461d-134">Default Documents String Array</span></span>

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

### <span data-ttu-id="1461d-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1461d-135">-DefaultProfile</span></span>
<span data-ttu-id="1461d-136">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1461d-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1461d-137">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="1461d-137">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="1461d-138">Detaljerad fel loggning aktiverat boolesk</span><span class="sxs-lookup"><span data-stu-id="1461d-138">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="1461d-139">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="1461d-139">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="1461d-140">Aktiverar/inaktiverar kontinuerlig distribution av behållare webhook</span><span class="sxs-lookup"><span data-stu-id="1461d-140">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="1461d-141">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="1461d-141">-HandlerMappings</span></span>
<span data-ttu-id="1461d-142">Hanterar mappningar IList</span><span class="sxs-lookup"><span data-stu-id="1461d-142">Handler Mappings IList</span></span>

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

### <span data-ttu-id="1461d-143">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="1461d-143">-HttpLoggingEnabled</span></span>
<span data-ttu-id="1461d-144">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="1461d-144">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="1461d-145">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="1461d-145">-HttpsOnly</span></span>
<span data-ttu-id="1461d-146">Aktivera/inaktivera all trafik till HTTPS på en befintlig plats</span><span class="sxs-lookup"><span data-stu-id="1461d-146">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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

### <span data-ttu-id="1461d-147">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="1461d-147">-ManagedPipelineMode</span></span>
<span data-ttu-id="1461d-148">Namn på hanterat pipeline-läge</span><span class="sxs-lookup"><span data-stu-id="1461d-148">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="1461d-149">-Namn</span><span class="sxs-lookup"><span data-stu-id="1461d-149">-Name</span></span>
<span data-ttu-id="1461d-150">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="1461d-150">WebApp Name</span></span>

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

### <span data-ttu-id="1461d-151">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="1461d-151">-NetFrameworkVersion</span></span>
<span data-ttu-id="1461d-152">NET Framework-version</span><span class="sxs-lookup"><span data-stu-id="1461d-152">Net Framework Version</span></span>

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

### <span data-ttu-id="1461d-153">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="1461d-153">-NumberOfWorkers</span></span>
<span data-ttu-id="1461d-154">Antalet arbetare som ska tilldelas</span><span class="sxs-lookup"><span data-stu-id="1461d-154">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="1461d-155">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="1461d-155">-PhpVersion</span></span>
<span data-ttu-id="1461d-156">Php-version</span><span class="sxs-lookup"><span data-stu-id="1461d-156">Php Version</span></span>

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

### <span data-ttu-id="1461d-157">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="1461d-157">-RequestTracingEnabled</span></span>
<span data-ttu-id="1461d-158">Begäran om spårning aktiverat boolesk</span><span class="sxs-lookup"><span data-stu-id="1461d-158">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="1461d-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1461d-159">-ResourceGroupName</span></span>
<span data-ttu-id="1461d-160">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="1461d-160">Resource Group Name</span></span>

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

### <span data-ttu-id="1461d-161">-Plats</span><span class="sxs-lookup"><span data-stu-id="1461d-161">-Slot</span></span>
<span data-ttu-id="1461d-162">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="1461d-162">WebApp Slot Name</span></span>

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

### <span data-ttu-id="1461d-163">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="1461d-163">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="1461d-164">Använda 32-bitars boolesk arbets process</span><span class="sxs-lookup"><span data-stu-id="1461d-164">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="1461d-165">-WebApp</span><span class="sxs-lookup"><span data-stu-id="1461d-165">-WebApp</span></span>
<span data-ttu-id="1461d-166">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="1461d-166">WebApp Object</span></span>

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

### <span data-ttu-id="1461d-167">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="1461d-167">-WebSocketsEnabled</span></span>
<span data-ttu-id="1461d-168">Boolesk aktiverat Boolean</span><span class="sxs-lookup"><span data-stu-id="1461d-168">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="1461d-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1461d-169">CommonParameters</span></span>
<span data-ttu-id="1461d-170">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1461d-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1461d-171">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1461d-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1461d-172">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1461d-172">INPUTS</span></span>

### <span data-ttu-id="1461d-173">System. Int32</span><span class="sxs-lookup"><span data-stu-id="1461d-173">System.Int32</span></span>
<span data-ttu-id="1461d-174">Parametrar: NumberOfWorkers (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1461d-174">Parameters: NumberOfWorkers (ByValue)</span></span>

### <span data-ttu-id="1461d-175">System. String</span><span class="sxs-lookup"><span data-stu-id="1461d-175">System.String</span></span>

### <span data-ttu-id="1461d-176">Microsoft. Azure. Management. webbplatser. Models. site</span><span class="sxs-lookup"><span data-stu-id="1461d-176">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="1461d-177">Parametrar: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1461d-177">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="1461d-178">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1461d-178">OUTPUTS</span></span>

### <span data-ttu-id="1461d-179">Microsoft. Azure. Management. webbplatser. Models. site</span><span class="sxs-lookup"><span data-stu-id="1461d-179">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="1461d-180">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1461d-180">NOTES</span></span>

## <span data-ttu-id="1461d-181">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1461d-181">RELATED LINKS</span></span>

[<span data-ttu-id="1461d-182">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="1461d-182">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="1461d-183">New-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="1461d-183">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="1461d-184">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="1461d-184">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="1461d-185">Restart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="1461d-185">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="1461d-186">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="1461d-186">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="1461d-187">Stopp-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="1461d-187">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="1461d-188">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="1461d-188">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)
