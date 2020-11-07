---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebappslot
schema: 2.0.0
ms.openlocfilehash: 245ce5ab011f03b8d8331b5d80fa4eeb01e19e15
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930762"
---
# <span data-ttu-id="573e3-101">Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="573e3-101">Set-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="573e3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="573e3-102">SYNOPSIS</span></span>
<span data-ttu-id="573e3-103">Ändrar en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="573e3-103">Modifies an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="573e3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="573e3-104">SYNTAX</span></span>

### <span data-ttu-id="573e3-105">S</span><span class="sxs-lookup"><span data-stu-id="573e3-105">S1</span></span>
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-ResourceGroupName] <String> [-Name] <String>
 [[-AssignIdentity] <Boolean>] [[HttpsOnly] <Boolean>] [-Slot] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="573e3-106">S2</span><span class="sxs-lookup"><span data-stu-id="573e3-106">S2</span></span>
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-WebApp] <Site> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="573e3-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="573e3-107">DESCRIPTION</span></span>
<span data-ttu-id="573e3-108">Cmdleten **set-AzureRmWebApp** anger en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="573e3-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="573e3-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="573e3-109">EXAMPLES</span></span>

### <span data-ttu-id="573e3-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="573e3-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="573e3-111">Det här kommandot anger HttpLoggingEnabled till sant för fack Slot001 som hör till Web App-ContosoWebApp som är kopplad till resurs gruppens standard-väst</span><span class="sxs-lookup"><span data-stu-id="573e3-111">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="573e3-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="573e3-112">PARAMETERS</span></span>

### <span data-ttu-id="573e3-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="573e3-113">-AppServicePlan</span></span>
<span data-ttu-id="573e3-114">Namn på App Service-abonnemang</span><span class="sxs-lookup"><span data-stu-id="573e3-114">App Service Plan Name</span></span>

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

### <span data-ttu-id="573e3-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="573e3-115">-AppSettings</span></span>
<span data-ttu-id="573e3-116">App Settings-hash</span><span class="sxs-lookup"><span data-stu-id="573e3-116">App Settings HashTable</span></span>

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

### <span data-ttu-id="573e3-117">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="573e3-117">-AutoSwapSlotName</span></span>
<span data-ttu-id="573e3-118">Mål plats namn för automatisk växling</span><span class="sxs-lookup"><span data-stu-id="573e3-118">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="573e3-119">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="573e3-119">-ConnectionStrings</span></span>
<span data-ttu-id="573e3-120">Anslutnings strängar-hash</span><span class="sxs-lookup"><span data-stu-id="573e3-120">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="573e3-121">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="573e3-121">-DefaultDocuments</span></span>
<span data-ttu-id="573e3-122">Matris för standard dokument</span><span class="sxs-lookup"><span data-stu-id="573e3-122">Default Documents String Array</span></span>

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

### <span data-ttu-id="573e3-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="573e3-123">-DefaultProfile</span></span>
<span data-ttu-id="573e3-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="573e3-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="573e3-125">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="573e3-125">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="573e3-126">Detaljerad fel loggning aktiverat boolesk</span><span class="sxs-lookup"><span data-stu-id="573e3-126">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="573e3-127">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="573e3-127">-HandlerMappings</span></span>
<span data-ttu-id="573e3-128">Hanterar mappningar IList</span><span class="sxs-lookup"><span data-stu-id="573e3-128">Handler Mappings IList</span></span>

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

### <span data-ttu-id="573e3-129">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="573e3-129">-HttpLoggingEnabled</span></span>
<span data-ttu-id="573e3-130">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="573e3-130">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="573e3-131">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="573e3-131">-ManagedPipelineMode</span></span>
<span data-ttu-id="573e3-132">Namn på hanterat pipeline-läge</span><span class="sxs-lookup"><span data-stu-id="573e3-132">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="573e3-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="573e3-133">-Name</span></span>
<span data-ttu-id="573e3-134">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="573e3-134">WebApp Name</span></span>

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

### <span data-ttu-id="573e3-135">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="573e3-135">-NetFrameworkVersion</span></span>
<span data-ttu-id="573e3-136">NET Framework-version</span><span class="sxs-lookup"><span data-stu-id="573e3-136">Net Framework Version</span></span>

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

### <span data-ttu-id="573e3-137">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="573e3-137">-NumberOfWorkers</span></span>
<span data-ttu-id="573e3-138">Antalet arbetare som ska tilldelas</span><span class="sxs-lookup"><span data-stu-id="573e3-138">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="573e3-139">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="573e3-139">-PhpVersion</span></span>
<span data-ttu-id="573e3-140">Php-version</span><span class="sxs-lookup"><span data-stu-id="573e3-140">Php Version</span></span>

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

### <span data-ttu-id="573e3-141">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="573e3-141">-RequestTracingEnabled</span></span>
<span data-ttu-id="573e3-142">Begäran om spårning aktiverat boolesk</span><span class="sxs-lookup"><span data-stu-id="573e3-142">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="573e3-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="573e3-143">-ResourceGroupName</span></span>
<span data-ttu-id="573e3-144">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="573e3-144">Resource Group Name</span></span>

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

### <span data-ttu-id="573e3-145">-Plats</span><span class="sxs-lookup"><span data-stu-id="573e3-145">-Slot</span></span>
<span data-ttu-id="573e3-146">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="573e3-146">WebApp Slot Name</span></span>

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

### <span data-ttu-id="573e3-147">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="573e3-147">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="573e3-148">Använda 32-bitars boolesk arbets process</span><span class="sxs-lookup"><span data-stu-id="573e3-148">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="573e3-149">-WebApp</span><span class="sxs-lookup"><span data-stu-id="573e3-149">-WebApp</span></span>
<span data-ttu-id="573e3-150">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="573e3-150">WebApp Object</span></span>

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

### <span data-ttu-id="573e3-151">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="573e3-151">-WebSocketsEnabled</span></span>
<span data-ttu-id="573e3-152">Boolesk aktiverat Boolean</span><span class="sxs-lookup"><span data-stu-id="573e3-152">Web Sockets Enabled Boolean</span></span>

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
### <span data-ttu-id="573e3-153">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="573e3-153">-HttpsOnly</span></span>
<span data-ttu-id="573e3-154">Aktivera/inaktivera all trafik till HTTPS på en befintlig plats</span><span class="sxs-lookup"><span data-stu-id="573e3-154">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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
### <span data-ttu-id="573e3-155">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="573e3-155">-AssignIdentity</span></span>
<span data-ttu-id="573e3-156">Aktivera/inaktivera MSI på en befintlig plats [för hands version]</span><span class="sxs-lookup"><span data-stu-id="573e3-156">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="573e3-157">-AsJob</span><span class="sxs-lookup"><span data-stu-id="573e3-157">-AsJob</span></span>
<span data-ttu-id="573e3-158">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="573e3-158">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="573e3-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="573e3-159">CommonParameters</span></span>
<span data-ttu-id="573e3-160">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="573e3-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="573e3-161">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="573e3-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="573e3-162">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="573e3-162">INPUTS</span></span>

### <span data-ttu-id="573e3-163">Int32</span><span class="sxs-lookup"><span data-stu-id="573e3-163">Int32</span></span>
<span data-ttu-id="573e3-164">Parametern ' NumberOfWorkers ' godkänner värdet för typen ' Int32 ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="573e3-164">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="573e3-165">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="573e3-165">Site</span></span>
<span data-ttu-id="573e3-166">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="573e3-166">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="573e3-167">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="573e3-167">OUTPUTS</span></span>

## <span data-ttu-id="573e3-168">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="573e3-168">NOTES</span></span>

## <span data-ttu-id="573e3-169">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="573e3-169">RELATED LINKS</span></span>

[<span data-ttu-id="573e3-170">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="573e3-170">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="573e3-171">New-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="573e3-171">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="573e3-172">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="573e3-172">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="573e3-173">Restart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="573e3-173">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="573e3-174">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="573e3-174">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="573e3-175">Stopp-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="573e3-175">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="573e3-176">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="573e3-176">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)
