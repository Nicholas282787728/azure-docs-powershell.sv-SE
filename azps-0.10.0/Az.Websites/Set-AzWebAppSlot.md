---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/set-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzWebAppSlot.md
ms.openlocfilehash: b6cb41e49695fa7fd9fa0efdefdbefb2b23229a5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923257"
---
# <span data-ttu-id="70d3d-101">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="70d3d-101">Set-AzWebAppSlot</span></span>

## <span data-ttu-id="70d3d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="70d3d-102">SYNOPSIS</span></span>
<span data-ttu-id="70d3d-103">Ändrar en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="70d3d-103">Modifies an Azure Web App slot.</span></span>

## <span data-ttu-id="70d3d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="70d3d-104">SYNTAX</span></span>

### <span data-ttu-id="70d3d-105">S</span><span class="sxs-lookup"><span data-stu-id="70d3d-105">S1</span></span>
```
Set-AzWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-ResourceGroupName] <String> [-Name] <String>
 [[-AssignIdentity] <Boolean>] [[HttpsOnly] <Boolean>] [-Slot] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70d3d-106">S2</span><span class="sxs-lookup"><span data-stu-id="70d3d-106">S2</span></span>
```
Set-AzWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-WebApp] <Site> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70d3d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="70d3d-107">DESCRIPTION</span></span>
<span data-ttu-id="70d3d-108">Cmdleten **set-AzWebApp** anger en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="70d3d-108">The **Set-AzWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="70d3d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="70d3d-109">EXAMPLES</span></span>

### <span data-ttu-id="70d3d-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="70d3d-110">Example 1</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="70d3d-111">Det här kommandot anger HttpLoggingEnabled till sant för fack Slot001 som hör till Web App-ContosoWebApp som är kopplad till resurs gruppens standard-väst</span><span class="sxs-lookup"><span data-stu-id="70d3d-111">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="70d3d-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="70d3d-112">PARAMETERS</span></span>

### <span data-ttu-id="70d3d-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="70d3d-113">-AppServicePlan</span></span>
<span data-ttu-id="70d3d-114">Namn på App Service-abonnemang</span><span class="sxs-lookup"><span data-stu-id="70d3d-114">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70d3d-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="70d3d-115">-AppSettings</span></span>
<span data-ttu-id="70d3d-116">App Settings-hash</span><span class="sxs-lookup"><span data-stu-id="70d3d-116">App Settings HashTable</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70d3d-117">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="70d3d-117">-AutoSwapSlotName</span></span>
<span data-ttu-id="70d3d-118">Mål plats namn för automatisk växling</span><span class="sxs-lookup"><span data-stu-id="70d3d-118">Destination slot name for auto swap</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70d3d-119">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="70d3d-119">-ConnectionStrings</span></span>
<span data-ttu-id="70d3d-120">Anslutnings strängar-hash</span><span class="sxs-lookup"><span data-stu-id="70d3d-120">Connection Strings HashTable</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70d3d-121">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="70d3d-121">-DefaultDocuments</span></span>
<span data-ttu-id="70d3d-122">Matris för standard dokument</span><span class="sxs-lookup"><span data-stu-id="70d3d-122">Default Documents String Array</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70d3d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70d3d-123">-DefaultProfile</span></span>
<span data-ttu-id="70d3d-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="70d3d-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70d3d-125">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="70d3d-125">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="70d3d-126">Detaljerad fel loggning aktiverat boolesk</span><span class="sxs-lookup"><span data-stu-id="70d3d-126">Detailed Error Logging Enabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70d3d-127">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="70d3d-127">-HandlerMappings</span></span>
<span data-ttu-id="70d3d-128">Hanterar mappningar IList</span><span class="sxs-lookup"><span data-stu-id="70d3d-128">Handler Mappings IList</span></span>

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

### <span data-ttu-id="70d3d-129">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="70d3d-129">-HttpLoggingEnabled</span></span>
<span data-ttu-id="70d3d-130">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="70d3d-130">HttpLoggingEnabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70d3d-131">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="70d3d-131">-ManagedPipelineMode</span></span>
<span data-ttu-id="70d3d-132">Namn på hanterat pipeline-läge</span><span class="sxs-lookup"><span data-stu-id="70d3d-132">Managed Pipeline Mode Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Classic, Integrated

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70d3d-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="70d3d-133">-Name</span></span>
<span data-ttu-id="70d3d-134">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="70d3d-134">WebApp Name</span></span>

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

### <span data-ttu-id="70d3d-135">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="70d3d-135">-NetFrameworkVersion</span></span>
<span data-ttu-id="70d3d-136">NET Framework-version</span><span class="sxs-lookup"><span data-stu-id="70d3d-136">Net Framework Version</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70d3d-137">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="70d3d-137">-NumberOfWorkers</span></span>
<span data-ttu-id="70d3d-138">Antalet arbetare som ska tilldelas</span><span class="sxs-lookup"><span data-stu-id="70d3d-138">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="70d3d-139">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="70d3d-139">-PhpVersion</span></span>
<span data-ttu-id="70d3d-140">Php-version</span><span class="sxs-lookup"><span data-stu-id="70d3d-140">Php Version</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70d3d-141">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="70d3d-141">-RequestTracingEnabled</span></span>
<span data-ttu-id="70d3d-142">Begäran om spårning aktiverat boolesk</span><span class="sxs-lookup"><span data-stu-id="70d3d-142">Request Tracing Enabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70d3d-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70d3d-143">-ResourceGroupName</span></span>
<span data-ttu-id="70d3d-144">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="70d3d-144">Resource Group Name</span></span>

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

### <span data-ttu-id="70d3d-145">-Plats</span><span class="sxs-lookup"><span data-stu-id="70d3d-145">-Slot</span></span>
<span data-ttu-id="70d3d-146">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="70d3d-146">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70d3d-147">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="70d3d-147">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="70d3d-148">Använda 32-bitars boolesk arbets process</span><span class="sxs-lookup"><span data-stu-id="70d3d-148">Use 32-bit Worker Process Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70d3d-149">-WebApp</span><span class="sxs-lookup"><span data-stu-id="70d3d-149">-WebApp</span></span>
<span data-ttu-id="70d3d-150">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="70d3d-150">WebApp Object</span></span>

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

### <span data-ttu-id="70d3d-151">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="70d3d-151">-WebSocketsEnabled</span></span>
<span data-ttu-id="70d3d-152">Boolesk aktiverat Boolean</span><span class="sxs-lookup"><span data-stu-id="70d3d-152">Web Sockets Enabled Boolean</span></span>

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
### <span data-ttu-id="70d3d-153">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="70d3d-153">-HttpsOnly</span></span>
<span data-ttu-id="70d3d-154">Aktivera/inaktivera all trafik till HTTPS på en befintlig plats</span><span class="sxs-lookup"><span data-stu-id="70d3d-154">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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
### <span data-ttu-id="70d3d-155">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="70d3d-155">-AssignIdentity</span></span>
<span data-ttu-id="70d3d-156">Aktivera/inaktivera MSI på en befintlig plats [för hands version]</span><span class="sxs-lookup"><span data-stu-id="70d3d-156">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="70d3d-157">-AsJob</span><span class="sxs-lookup"><span data-stu-id="70d3d-157">-AsJob</span></span>
<span data-ttu-id="70d3d-158">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="70d3d-158">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="70d3d-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70d3d-159">CommonParameters</span></span>
<span data-ttu-id="70d3d-160">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70d3d-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70d3d-161">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70d3d-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70d3d-162">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="70d3d-162">INPUTS</span></span>

### <span data-ttu-id="70d3d-163">Int32</span><span class="sxs-lookup"><span data-stu-id="70d3d-163">Int32</span></span>
<span data-ttu-id="70d3d-164">Parametern ' NumberOfWorkers ' godkänner värdet för typen ' Int32 ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="70d3d-164">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="70d3d-165">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="70d3d-165">Site</span></span>
<span data-ttu-id="70d3d-166">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="70d3d-166">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="70d3d-167">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="70d3d-167">OUTPUTS</span></span>

## <span data-ttu-id="70d3d-168">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="70d3d-168">NOTES</span></span>

## <span data-ttu-id="70d3d-169">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="70d3d-169">RELATED LINKS</span></span>

[<span data-ttu-id="70d3d-170">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="70d3d-170">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="70d3d-171">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="70d3d-171">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="70d3d-172">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="70d3d-172">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="70d3d-173">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="70d3d-173">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="70d3d-174">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="70d3d-174">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="70d3d-175">Stopp-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="70d3d-175">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="70d3d-176">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="70d3d-176">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)
