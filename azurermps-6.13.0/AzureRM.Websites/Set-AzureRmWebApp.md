---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
ms.openlocfilehash: a47f490ae77fc540f3e14708b19dade5ce4e7c3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576721"
---
# <span data-ttu-id="a4d54-101">Set-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="a4d54-101">Set-AzureRmWebApp</span></span>

## <span data-ttu-id="a4d54-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a4d54-102">SYNOPSIS</span></span>
<span data-ttu-id="a4d54-103">Ändrar ett Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="a4d54-103">Modifies an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4d54-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a4d54-104">SYNTAX</span></span>

### <span data-ttu-id="a4d54-105">S</span><span class="sxs-lookup"><span data-stu-id="a4d54-105">S1</span></span>
```
Set-AzureRmWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [[-AutoSwapSlotName] <String>] [-ContainerImageName <String>] [-ContainerRegistryUrl <String>]
 [-ContainerRegistryUser <String>] [-ContainerRegistryPassword <SecureString>]
 [-EnableContainerContinuousDeployment <Boolean>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>] [-AsJob]
 [-AssignIdentity <Boolean>] [-HttpsOnly <Boolean>] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4d54-106">S2</span><span class="sxs-lookup"><span data-stu-id="a4d54-106">S2</span></span>
```
Set-AzureRmWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>]
 [-NumberOfWorkers <Int32>] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a4d54-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a4d54-107">DESCRIPTION</span></span>
<span data-ttu-id="a4d54-108">Cmdleten **set-AzureRmWebApp** anger en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="a4d54-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="a4d54-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a4d54-109">EXAMPLES</span></span>

### <span data-ttu-id="a4d54-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a4d54-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="a4d54-111">Det här kommandot anger HttpLoggingEnabled till sant för Web App-ContosoWebApp som är kopplat till resurs gruppens standard-väst</span><span class="sxs-lookup"><span data-stu-id="a4d54-111">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="a4d54-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a4d54-112">PARAMETERS</span></span>

### <span data-ttu-id="a4d54-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a4d54-113">-AppServicePlan</span></span>
<span data-ttu-id="a4d54-114">Namn på App Service-abonnemang</span><span class="sxs-lookup"><span data-stu-id="a4d54-114">App Service Plan Name</span></span>

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

### <span data-ttu-id="a4d54-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="a4d54-115">-AppSettings</span></span>
<span data-ttu-id="a4d54-116">App Settings-hash</span><span class="sxs-lookup"><span data-stu-id="a4d54-116">App Settings HashTable</span></span>

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

### <span data-ttu-id="a4d54-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a4d54-117">-AsJob</span></span>
<span data-ttu-id="a4d54-118">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="a4d54-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a4d54-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="a4d54-119">-AssignIdentity</span></span>
<span data-ttu-id="a4d54-120">Aktivera/inaktivera MSI på en befintlig Azure webapp eller functionapp</span><span class="sxs-lookup"><span data-stu-id="a4d54-120">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="a4d54-121">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="a4d54-121">-AutoSwapSlotName</span></span>
<span data-ttu-id="a4d54-122">Mål plats namn för automatisk växling</span><span class="sxs-lookup"><span data-stu-id="a4d54-122">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="a4d54-123">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="a4d54-123">-ConnectionStrings</span></span>
<span data-ttu-id="a4d54-124">Anslutnings strängar-hash</span><span class="sxs-lookup"><span data-stu-id="a4d54-124">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="a4d54-125">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="a4d54-125">-ContainerImageName</span></span>
<span data-ttu-id="a4d54-126">Bild namn för behållare</span><span class="sxs-lookup"><span data-stu-id="a4d54-126">Container Image Name</span></span>

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

### <span data-ttu-id="a4d54-127">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="a4d54-127">-ContainerRegistryPassword</span></span>
<span data-ttu-id="a4d54-128">Lösen ord för privat behållare</span><span class="sxs-lookup"><span data-stu-id="a4d54-128">Private Container Registry Password</span></span>

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

### <span data-ttu-id="a4d54-129">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="a4d54-129">-ContainerRegistryUrl</span></span>
<span data-ttu-id="a4d54-130">Webb adress för privat behållarens register Server</span><span class="sxs-lookup"><span data-stu-id="a4d54-130">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="a4d54-131">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="a4d54-131">-ContainerRegistryUser</span></span>
<span data-ttu-id="a4d54-132">Användar namn för privat behållare</span><span class="sxs-lookup"><span data-stu-id="a4d54-132">Private Container Registry Username</span></span>

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

### <span data-ttu-id="a4d54-133">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="a4d54-133">-DefaultDocuments</span></span>
<span data-ttu-id="a4d54-134">Matris för standard dokument</span><span class="sxs-lookup"><span data-stu-id="a4d54-134">Default Documents String Array</span></span>

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

### <span data-ttu-id="a4d54-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4d54-135">-DefaultProfile</span></span>
<span data-ttu-id="a4d54-136">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a4d54-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4d54-137">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="a4d54-137">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="a4d54-138">Detaljerad fel loggning aktiverat boolesk</span><span class="sxs-lookup"><span data-stu-id="a4d54-138">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="a4d54-139">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="a4d54-139">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="a4d54-140">Aktiverar/inaktiverar kontinuerlig distribution av behållare webhook</span><span class="sxs-lookup"><span data-stu-id="a4d54-140">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="a4d54-141">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="a4d54-141">-HandlerMappings</span></span>
<span data-ttu-id="a4d54-142">Hanterar mappningar IList</span><span class="sxs-lookup"><span data-stu-id="a4d54-142">Handler Mappings IList</span></span>

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

### <span data-ttu-id="a4d54-143">-Värdnamn</span><span class="sxs-lookup"><span data-stu-id="a4d54-143">-HostNames</span></span>
<span data-ttu-id="a4d54-144">Matris för WebApp-värdnamn</span><span class="sxs-lookup"><span data-stu-id="a4d54-144">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="a4d54-145">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="a4d54-145">-HttpLoggingEnabled</span></span>
<span data-ttu-id="a4d54-146">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="a4d54-146">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="a4d54-147">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="a4d54-147">-HttpsOnly</span></span>
<span data-ttu-id="a4d54-148">Aktivera/inaktivera omdirigering av all trafik till HTTPS på en befintlig Azure webapp eller functionapp</span><span class="sxs-lookup"><span data-stu-id="a4d54-148">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="a4d54-149">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="a4d54-149">-ManagedPipelineMode</span></span>
<span data-ttu-id="a4d54-150">Namn på hanterat pipeline-läge</span><span class="sxs-lookup"><span data-stu-id="a4d54-150">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="a4d54-151">-Namn</span><span class="sxs-lookup"><span data-stu-id="a4d54-151">-Name</span></span>
<span data-ttu-id="a4d54-152">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="a4d54-152">WebApp Name</span></span>

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

### <span data-ttu-id="a4d54-153">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="a4d54-153">-NetFrameworkVersion</span></span>
<span data-ttu-id="a4d54-154">NET Framework-version</span><span class="sxs-lookup"><span data-stu-id="a4d54-154">Net Framework Version</span></span>

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

### <span data-ttu-id="a4d54-155">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="a4d54-155">-NumberOfWorkers</span></span>
<span data-ttu-id="a4d54-156">Antalet arbetare som ska tilldelas</span><span class="sxs-lookup"><span data-stu-id="a4d54-156">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="a4d54-157">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="a4d54-157">-PhpVersion</span></span>
<span data-ttu-id="a4d54-158">Php-version</span><span class="sxs-lookup"><span data-stu-id="a4d54-158">Php Version</span></span>

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

### <span data-ttu-id="a4d54-159">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="a4d54-159">-RequestTracingEnabled</span></span>
<span data-ttu-id="a4d54-160">Begäran om spårning aktive rad</span><span class="sxs-lookup"><span data-stu-id="a4d54-160">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="a4d54-161">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4d54-161">-ResourceGroupName</span></span>
<span data-ttu-id="a4d54-162">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="a4d54-162">Resource Group Name</span></span>

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

### <span data-ttu-id="a4d54-163">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="a4d54-163">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="a4d54-164">Använda 32-bitars boolesk arbets process</span><span class="sxs-lookup"><span data-stu-id="a4d54-164">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="a4d54-165">-WebApp</span><span class="sxs-lookup"><span data-stu-id="a4d54-165">-WebApp</span></span>
<span data-ttu-id="a4d54-166">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="a4d54-166">WebApp Object</span></span>

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

### <span data-ttu-id="a4d54-167">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="a4d54-167">-WebSocketsEnabled</span></span>
<span data-ttu-id="a4d54-168">WebSocketsEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="a4d54-168">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="a4d54-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4d54-169">CommonParameters</span></span>
<span data-ttu-id="a4d54-170">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4d54-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4d54-171">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4d54-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4d54-172">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a4d54-172">INPUTS</span></span>

### <span data-ttu-id="a4d54-173">System. Int32</span><span class="sxs-lookup"><span data-stu-id="a4d54-173">System.Int32</span></span>
<span data-ttu-id="a4d54-174">Parametrar: NumberOfWorkers (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a4d54-174">Parameters: NumberOfWorkers (ByValue)</span></span>

### <span data-ttu-id="a4d54-175">System. String</span><span class="sxs-lookup"><span data-stu-id="a4d54-175">System.String</span></span>

### <span data-ttu-id="a4d54-176">Microsoft. Azure. Management. webbplatser. Models. site</span><span class="sxs-lookup"><span data-stu-id="a4d54-176">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="a4d54-177">Parametrar: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a4d54-177">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="a4d54-178">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a4d54-178">OUTPUTS</span></span>

### <span data-ttu-id="a4d54-179">Microsoft. Azure. Management. webbplatser. Models. site</span><span class="sxs-lookup"><span data-stu-id="a4d54-179">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="a4d54-180">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a4d54-180">NOTES</span></span>

## <span data-ttu-id="a4d54-181">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a4d54-181">RELATED LINKS</span></span>

[<span data-ttu-id="a4d54-182">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="a4d54-182">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="a4d54-183">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="a4d54-183">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="a4d54-184">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="a4d54-184">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="a4d54-185">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="a4d54-185">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="a4d54-186">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="a4d54-186">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="a4d54-187">Stopp-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="a4d54-187">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)
