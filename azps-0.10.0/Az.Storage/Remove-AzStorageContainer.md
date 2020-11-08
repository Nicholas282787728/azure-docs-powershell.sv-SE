---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6A46DA60-2ACF-4842-B5B3-58944264854A
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Remove-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Remove-AzStorageContainer.md
ms.openlocfilehash: 6f1d2c966ebd80d350b77401fee00aaf547cd932
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923533"
---
# <span data-ttu-id="87e18-101">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="87e18-101">Remove-AzStorageContainer</span></span>

## <span data-ttu-id="87e18-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="87e18-102">SYNOPSIS</span></span>
<span data-ttu-id="87e18-103">Tar bort den angivna lagrings behållaren.</span><span class="sxs-lookup"><span data-stu-id="87e18-103">Removes the specified storage container.</span></span>

## <span data-ttu-id="87e18-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="87e18-104">SYNTAX</span></span>

```
Remove-AzStorageContainer [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="87e18-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="87e18-105">DESCRIPTION</span></span>
<span data-ttu-id="87e18-106">Cmdleten **Remove-AzStorageContainer** tar bort den angivna lagrings behållaren i Azure.</span><span class="sxs-lookup"><span data-stu-id="87e18-106">The **Remove-AzStorageContainer** cmdlet removes the specified storage container in Azure.</span></span>

## <span data-ttu-id="87e18-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="87e18-107">EXAMPLES</span></span>

### <span data-ttu-id="87e18-108">Exempel 1: ta bort en behållare</span><span class="sxs-lookup"><span data-stu-id="87e18-108">Example 1: Remove a container</span></span>
```
PS C:\>Remove-AzStorageContainer -Name "MyTestContainer"
```

<span data-ttu-id="87e18-109">I det här exemplet tas en container bort med namnet MyTestContainer.</span><span class="sxs-lookup"><span data-stu-id="87e18-109">This example removes a container named MyTestContainer.</span></span>

## <span data-ttu-id="87e18-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="87e18-110">PARAMETERS</span></span>

### <span data-ttu-id="87e18-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="87e18-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="87e18-112">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="87e18-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="87e18-113">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="87e18-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="87e18-114">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="87e18-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87e18-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="87e18-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="87e18-116">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="87e18-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="87e18-117">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="87e18-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="87e18-118">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="87e18-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="87e18-119">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="87e18-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="87e18-120">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="87e18-120">The default value is 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87e18-121">-Kontext</span><span class="sxs-lookup"><span data-stu-id="87e18-121">-Context</span></span>
<span data-ttu-id="87e18-122">Anger en kontext för den behållare som du vill ta bort.</span><span class="sxs-lookup"><span data-stu-id="87e18-122">Specifies a context for the container you want to remove.</span></span>
<span data-ttu-id="87e18-123">Du kan använda New-AzStorageContext cmdlet för att skapa den.</span><span class="sxs-lookup"><span data-stu-id="87e18-123">You can use the New-AzStorageContext cmdlet to create it.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87e18-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87e18-124">-DefaultProfile</span></span>
<span data-ttu-id="87e18-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="87e18-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87e18-126">-Force</span><span class="sxs-lookup"><span data-stu-id="87e18-126">-Force</span></span>
<span data-ttu-id="87e18-127">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="87e18-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="87e18-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="87e18-128">-Name</span></span>
<span data-ttu-id="87e18-129">Anger namnet på den behållare som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="87e18-129">Specifies the name of the container to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87e18-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="87e18-130">-PassThru</span></span>
<span data-ttu-id="87e18-131">Anger att denna cmdlet returnerar ett **booleskt** värde som visar att åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="87e18-131">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="87e18-132">Denna cmdlet returnerar som standard inget värde.</span><span class="sxs-lookup"><span data-stu-id="87e18-132">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="87e18-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="87e18-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="87e18-134">Anger timeout-intervall för tjänsten i sekunder för en begäran.</span><span class="sxs-lookup"><span data-stu-id="87e18-134">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="87e18-135">Om det angivna intervallet förflyter innan tjänsten bearbetar begäran returnerar lagrings tjänsten ett fel.</span><span class="sxs-lookup"><span data-stu-id="87e18-135">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87e18-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="87e18-136">-Confirm</span></span>
<span data-ttu-id="87e18-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="87e18-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87e18-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87e18-138">-WhatIf</span></span>
<span data-ttu-id="87e18-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="87e18-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87e18-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="87e18-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87e18-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87e18-141">CommonParameters</span></span>
<span data-ttu-id="87e18-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87e18-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87e18-143">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87e18-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87e18-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="87e18-144">INPUTS</span></span>

### <span data-ttu-id="87e18-145">System. String</span><span class="sxs-lookup"><span data-stu-id="87e18-145">System.String</span></span>

### <span data-ttu-id="87e18-146">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="87e18-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="87e18-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="87e18-147">OUTPUTS</span></span>

### <span data-ttu-id="87e18-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="87e18-148">System.Boolean</span></span>

## <span data-ttu-id="87e18-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="87e18-149">NOTES</span></span>

## <span data-ttu-id="87e18-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="87e18-150">RELATED LINKS</span></span>

[<span data-ttu-id="87e18-151">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="87e18-151">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="87e18-152">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="87e18-152">New-AzStorageContainer</span></span>](./New-AzStorageContainer.md)