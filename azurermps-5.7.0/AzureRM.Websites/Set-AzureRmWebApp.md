---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
ms.openlocfilehash: 3587c7a725386976a04a9dc9922b3b0a16eb9362
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582883"
---
# <span data-ttu-id="46287-101">Set-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="46287-101">Set-AzureRmWebApp</span></span>

## <span data-ttu-id="46287-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="46287-102">SYNOPSIS</span></span>
<span data-ttu-id="46287-103">Ändrar ett Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="46287-103">Modifies an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46287-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="46287-104">SYNTAX</span></span>

### <span data-ttu-id="46287-105">S</span><span class="sxs-lookup"><span data-stu-id="46287-105">S1</span></span>
```
Set-AzureRmWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [[-AutoSwapSlotName] <String>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>]
 [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46287-106">S2</span><span class="sxs-lookup"><span data-stu-id="46287-106">S2</span></span>
```
Set-AzureRmWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>]
 [-NumberOfWorkers <Int32>] [-WebApp] <Site> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46287-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="46287-107">DESCRIPTION</span></span>
<span data-ttu-id="46287-108">Cmdleten **set-AzureRmWebApp** anger en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="46287-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="46287-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="46287-109">EXAMPLES</span></span>

### <span data-ttu-id="46287-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="46287-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="46287-111">Det här kommandot anger HttpLoggingEnabled till sant för Web App-ContosoWebApp som är kopplat till resurs gruppens standard-väst</span><span class="sxs-lookup"><span data-stu-id="46287-111">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="46287-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="46287-112">PARAMETERS</span></span>

### <span data-ttu-id="46287-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="46287-113">-AppServicePlan</span></span>
<span data-ttu-id="46287-114">Namn på App Service-abonnemang</span><span class="sxs-lookup"><span data-stu-id="46287-114">App Service Plan Name</span></span>

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

### <span data-ttu-id="46287-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="46287-115">-AppSettings</span></span>
<span data-ttu-id="46287-116">App Settings-hash</span><span class="sxs-lookup"><span data-stu-id="46287-116">App Settings HashTable</span></span>

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

### <span data-ttu-id="46287-117">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="46287-117">-AutoSwapSlotName</span></span>
<span data-ttu-id="46287-118">Mål plats namn för automatisk växling</span><span class="sxs-lookup"><span data-stu-id="46287-118">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="46287-119">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="46287-119">-ConnectionStrings</span></span>
<span data-ttu-id="46287-120">Anslutnings strängar-hash</span><span class="sxs-lookup"><span data-stu-id="46287-120">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="46287-121">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="46287-121">-DefaultDocuments</span></span>
<span data-ttu-id="46287-122">Matris för standard dokument</span><span class="sxs-lookup"><span data-stu-id="46287-122">Default Documents String Array</span></span>

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

### <span data-ttu-id="46287-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46287-123">-DefaultProfile</span></span>
<span data-ttu-id="46287-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="46287-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46287-125">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="46287-125">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="46287-126">Detaljerad fel loggning aktiverat boolesk</span><span class="sxs-lookup"><span data-stu-id="46287-126">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="46287-127">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="46287-127">-HandlerMappings</span></span>
<span data-ttu-id="46287-128">Hanterar mappningar IList</span><span class="sxs-lookup"><span data-stu-id="46287-128">Handler Mappings IList</span></span>

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

### <span data-ttu-id="46287-129">-Värdnamn</span><span class="sxs-lookup"><span data-stu-id="46287-129">-HostNames</span></span>
<span data-ttu-id="46287-130">Matris för WebApp-värdnamn</span><span class="sxs-lookup"><span data-stu-id="46287-130">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="46287-131">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="46287-131">-HttpLoggingEnabled</span></span>
<span data-ttu-id="46287-132">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="46287-132">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="46287-133">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="46287-133">-ManagedPipelineMode</span></span>
<span data-ttu-id="46287-134">Namn på hanterat pipeline-läge</span><span class="sxs-lookup"><span data-stu-id="46287-134">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="46287-135">-Namn</span><span class="sxs-lookup"><span data-stu-id="46287-135">-Name</span></span>
<span data-ttu-id="46287-136">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="46287-136">WebApp Name</span></span>

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

### <span data-ttu-id="46287-137">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="46287-137">-NetFrameworkVersion</span></span>
<span data-ttu-id="46287-138">NET Framework-version</span><span class="sxs-lookup"><span data-stu-id="46287-138">Net Framework Version</span></span>

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

### <span data-ttu-id="46287-139">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="46287-139">-NumberOfWorkers</span></span>
<span data-ttu-id="46287-140">Antalet arbetare som ska tilldelas</span><span class="sxs-lookup"><span data-stu-id="46287-140">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="46287-141">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="46287-141">-PhpVersion</span></span>
<span data-ttu-id="46287-142">Php-version</span><span class="sxs-lookup"><span data-stu-id="46287-142">Php Version</span></span>

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

### <span data-ttu-id="46287-143">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="46287-143">-RequestTracingEnabled</span></span>
<span data-ttu-id="46287-144">Begäran om spårning aktive rad</span><span class="sxs-lookup"><span data-stu-id="46287-144">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="46287-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46287-145">-ResourceGroupName</span></span>
<span data-ttu-id="46287-146">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="46287-146">Resource Group Name</span></span>

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

### <span data-ttu-id="46287-147">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="46287-147">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="46287-148">Använda 32-bitars boolesk arbets process</span><span class="sxs-lookup"><span data-stu-id="46287-148">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="46287-149">-WebApp</span><span class="sxs-lookup"><span data-stu-id="46287-149">-WebApp</span></span>
<span data-ttu-id="46287-150">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="46287-150">WebApp Object</span></span>

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

### <span data-ttu-id="46287-151">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="46287-151">-WebSocketsEnabled</span></span>
<span data-ttu-id="46287-152">WebSocketsEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="46287-152">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="46287-153">-AsJob</span><span class="sxs-lookup"><span data-stu-id="46287-153">-AsJob</span></span>
<span data-ttu-id="46287-154">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="46287-154">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="46287-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46287-155">CommonParameters</span></span>
<span data-ttu-id="46287-156">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46287-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46287-157">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46287-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46287-158">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="46287-158">INPUTS</span></span>

### <span data-ttu-id="46287-159">Int32</span><span class="sxs-lookup"><span data-stu-id="46287-159">Int32</span></span>
<span data-ttu-id="46287-160">Parametern ' NumberOfWorkers ' godkänner värdet för typen ' Int32 ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="46287-160">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="46287-161">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="46287-161">Site</span></span>
<span data-ttu-id="46287-162">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="46287-162">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="46287-163">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="46287-163">OUTPUTS</span></span>

## <span data-ttu-id="46287-164">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="46287-164">NOTES</span></span>

## <span data-ttu-id="46287-165">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="46287-165">RELATED LINKS</span></span>

[<span data-ttu-id="46287-166">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="46287-166">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="46287-167">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="46287-167">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="46287-168">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="46287-168">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="46287-169">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="46287-169">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="46287-170">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="46287-170">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="46287-171">Stopp-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="46287-171">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)
