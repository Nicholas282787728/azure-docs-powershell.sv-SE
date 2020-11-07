---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebapp
schema: 2.0.0
ms.openlocfilehash: d722c378e246fa175741c91092d99415275f094e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929538"
---
# <span data-ttu-id="9207e-101">Set-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="9207e-101">Set-AzureRmWebApp</span></span>

## <span data-ttu-id="9207e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9207e-102">SYNOPSIS</span></span>
<span data-ttu-id="9207e-103">Ändrar ett Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="9207e-103">Modifies an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9207e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9207e-104">SYNTAX</span></span>

### <span data-ttu-id="9207e-105">S</span><span class="sxs-lookup"><span data-stu-id="9207e-105">S1</span></span>
```
Set-AzureRmWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [[-AutoSwapSlotName] <String>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>] [-AsJob] [[-AssignIdentity] <Boolean>]
 [[-HttpsOnly] <Boolean>] [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9207e-106">S2</span><span class="sxs-lookup"><span data-stu-id="9207e-106">S2</span></span>
```
Set-AzureRmWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>]
 [-NumberOfWorkers <Int32>] [-AsJob] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9207e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9207e-107">DESCRIPTION</span></span>
<span data-ttu-id="9207e-108">Cmdleten **set-AzureRmWebApp** anger en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="9207e-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="9207e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9207e-109">EXAMPLES</span></span>

### <span data-ttu-id="9207e-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9207e-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="9207e-111">Det här kommandot anger HttpLoggingEnabled till sant för Web App-ContosoWebApp som är kopplat till resurs gruppens standard-väst</span><span class="sxs-lookup"><span data-stu-id="9207e-111">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="9207e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9207e-112">PARAMETERS</span></span>

### <span data-ttu-id="9207e-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9207e-113">-AppServicePlan</span></span>
<span data-ttu-id="9207e-114">Namn på App Service-abonnemang</span><span class="sxs-lookup"><span data-stu-id="9207e-114">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9207e-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="9207e-115">-AppSettings</span></span>
<span data-ttu-id="9207e-116">App Settings-hash</span><span class="sxs-lookup"><span data-stu-id="9207e-116">App Settings HashTable</span></span>

```yaml
Type: Hashtable
Parameter Sets: S1
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9207e-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9207e-117">-AsJob</span></span>
<span data-ttu-id="9207e-118">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="9207e-118">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9207e-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="9207e-119">-AssignIdentity</span></span>
<span data-ttu-id="9207e-120">Aktivera/inaktivera MSI på en befintlig Azure webapp eller functionapp [för hands version]</span><span class="sxs-lookup"><span data-stu-id="9207e-120">Enable/disable MSI on an existing azure webapp or functionapp [PREVIEW]</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9207e-121">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="9207e-121">-AutoSwapSlotName</span></span>
<span data-ttu-id="9207e-122">Mål plats namn för automatisk växling</span><span class="sxs-lookup"><span data-stu-id="9207e-122">Destination slot name for auto swap</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9207e-123">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="9207e-123">-ConnectionStrings</span></span>
<span data-ttu-id="9207e-124">Anslutnings strängar-hash</span><span class="sxs-lookup"><span data-stu-id="9207e-124">Connection Strings HashTable</span></span>

```yaml
Type: Hashtable
Parameter Sets: S1
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9207e-125">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="9207e-125">-DefaultDocuments</span></span>
<span data-ttu-id="9207e-126">Matris för standard dokument</span><span class="sxs-lookup"><span data-stu-id="9207e-126">Default Documents String Array</span></span>

```yaml
Type: String[]
Parameter Sets: S1
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9207e-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9207e-127">-DefaultProfile</span></span>
<span data-ttu-id="9207e-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9207e-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9207e-129">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="9207e-129">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="9207e-130">Detaljerad fel loggning aktiverat boolesk</span><span class="sxs-lookup"><span data-stu-id="9207e-130">Detailed Error Logging Enabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9207e-131">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="9207e-131">-HandlerMappings</span></span>
<span data-ttu-id="9207e-132">Hanterar mappningar IList</span><span class="sxs-lookup"><span data-stu-id="9207e-132">Handler Mappings IList</span></span>

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

### <span data-ttu-id="9207e-133">-Värdnamn</span><span class="sxs-lookup"><span data-stu-id="9207e-133">-HostNames</span></span>
<span data-ttu-id="9207e-134">Matris för WebApp-värdnamn</span><span class="sxs-lookup"><span data-stu-id="9207e-134">WebApp HostNames String Array</span></span>

```yaml
Type: String[]
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9207e-135">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="9207e-135">-HttpLoggingEnabled</span></span>
<span data-ttu-id="9207e-136">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="9207e-136">HttpLoggingEnabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9207e-137">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="9207e-137">-HttpsOnly</span></span>
<span data-ttu-id="9207e-138">Aktivera/inaktivera omdirigering av all trafik till HTTPS på en befintlig Azure webapp eller functionapp</span><span class="sxs-lookup"><span data-stu-id="9207e-138">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9207e-139">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="9207e-139">-ManagedPipelineMode</span></span>
<span data-ttu-id="9207e-140">Namn på hanterat pipeline-läge</span><span class="sxs-lookup"><span data-stu-id="9207e-140">Managed Pipeline Mode Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 
Accepted values: Classic, Integrated

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9207e-141">-Namn</span><span class="sxs-lookup"><span data-stu-id="9207e-141">-Name</span></span>
<span data-ttu-id="9207e-142">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="9207e-142">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9207e-143">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="9207e-143">-NetFrameworkVersion</span></span>
<span data-ttu-id="9207e-144">NET Framework-version</span><span class="sxs-lookup"><span data-stu-id="9207e-144">Net Framework Version</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9207e-145">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="9207e-145">-NumberOfWorkers</span></span>
<span data-ttu-id="9207e-146">Antalet arbetare som ska tilldelas</span><span class="sxs-lookup"><span data-stu-id="9207e-146">The number of workers to be allocated</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9207e-147">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="9207e-147">-PhpVersion</span></span>
<span data-ttu-id="9207e-148">Php-version</span><span class="sxs-lookup"><span data-stu-id="9207e-148">Php Version</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9207e-149">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="9207e-149">-RequestTracingEnabled</span></span>
<span data-ttu-id="9207e-150">Begäran om spårning aktive rad</span><span class="sxs-lookup"><span data-stu-id="9207e-150">Request Tracing Enabled</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9207e-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9207e-151">-ResourceGroupName</span></span>
<span data-ttu-id="9207e-152">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="9207e-152">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9207e-153">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="9207e-153">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="9207e-154">Använda 32-bitars boolesk arbets process</span><span class="sxs-lookup"><span data-stu-id="9207e-154">Use 32-bit Worker Process Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 14
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9207e-155">-WebApp</span><span class="sxs-lookup"><span data-stu-id="9207e-155">-WebApp</span></span>
<span data-ttu-id="9207e-156">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="9207e-156">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9207e-157">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="9207e-157">-WebSocketsEnabled</span></span>
<span data-ttu-id="9207e-158">WebSocketsEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="9207e-158">WebSocketsEnabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9207e-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9207e-159">CommonParameters</span></span>
<span data-ttu-id="9207e-160">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9207e-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9207e-161">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9207e-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9207e-162">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9207e-162">INPUTS</span></span>

### <span data-ttu-id="9207e-163">Int32</span><span class="sxs-lookup"><span data-stu-id="9207e-163">Int32</span></span>
<span data-ttu-id="9207e-164">Parametern ' NumberOfWorkers ' godkänner värdet för typen ' Int32 ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="9207e-164">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="9207e-165">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="9207e-165">Site</span></span>
<span data-ttu-id="9207e-166">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="9207e-166">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="9207e-167">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9207e-167">OUTPUTS</span></span>

## <span data-ttu-id="9207e-168">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9207e-168">NOTES</span></span>

## <span data-ttu-id="9207e-169">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9207e-169">RELATED LINKS</span></span>

[<span data-ttu-id="9207e-170">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="9207e-170">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="9207e-171">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="9207e-171">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="9207e-172">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="9207e-172">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="9207e-173">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="9207e-173">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="9207e-174">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="9207e-174">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="9207e-175">Stopp-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="9207e-175">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)
