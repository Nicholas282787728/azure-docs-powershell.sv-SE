---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E2CCDA8F-2D45-4F25-B297-337B7AB021E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: d8c9e0e49ba7a5caa9cb93290ef5e96b60fd4430
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94103396"
---
# <span data-ttu-id="3c598-101">Remove-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3c598-101">Remove-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="3c598-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3c598-102">SYNOPSIS</span></span>
<span data-ttu-id="3c598-103">Tar bort en lagrad åtkomst princip från en lagrings plats.</span><span class="sxs-lookup"><span data-stu-id="3c598-103">Removes a stored access policy from a Storage share.</span></span>

## <span data-ttu-id="3c598-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3c598-104">SYNTAX</span></span>

```
Remove-AzStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3c598-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3c598-105">DESCRIPTION</span></span>
<span data-ttu-id="3c598-106">Cmdleten **Remove-AzStorageShareStoredAccessPolicy** tar bort en lagrad åtkomst princip från en Azure Storage-resurs.</span><span class="sxs-lookup"><span data-stu-id="3c598-106">The **Remove-AzStorageShareStoredAccessPolicy** cmdlet removes a stored access policy from an Azure Storage share.</span></span>

## <span data-ttu-id="3c598-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3c598-107">EXAMPLES</span></span>

### <span data-ttu-id="3c598-108">Exempel 1: ta bort en lagrad åtkomst princip från en Azure-lagringsenhet</span><span class="sxs-lookup"><span data-stu-id="3c598-108">Example 1: Remove a stored access policy from an Azure Storage share</span></span>
```
PS C:\>Remove-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="3c598-109">Det här kommandot tar bort en lagrad åtkomst princip med namnet GeneralPolicy från ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="3c598-109">This command removes a stored access policy named GeneralPolicy from ContosoShare.</span></span>

## <span data-ttu-id="3c598-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3c598-110">PARAMETERS</span></span>

### <span data-ttu-id="3c598-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3c598-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="3c598-112">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="3c598-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="3c598-113">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="3c598-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="3c598-114">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="3c598-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c598-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="3c598-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="3c598-116">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="3c598-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="3c598-117">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="3c598-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="3c598-118">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="3c598-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="3c598-119">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="3c598-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="3c598-120">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="3c598-120">The default value is 10.</span></span>

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

### <span data-ttu-id="3c598-121">-Kontext</span><span class="sxs-lookup"><span data-stu-id="3c598-121">-Context</span></span>
<span data-ttu-id="3c598-122">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="3c598-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="3c598-123">Använd cmdleten [New-AzStorageContext](./New-AzStorageContext.md) för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="3c598-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="3c598-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c598-124">-DefaultProfile</span></span>
<span data-ttu-id="3c598-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3c598-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c598-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3c598-126">-PassThru</span></span>
<span data-ttu-id="3c598-127">Anger att denna cmdlet returnerar ett **booleskt** värde som visar att åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="3c598-127">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="3c598-128">Denna cmdlet returnerar som standard inget värde.</span><span class="sxs-lookup"><span data-stu-id="3c598-128">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="3c598-129">-Princip</span><span class="sxs-lookup"><span data-stu-id="3c598-129">-Policy</span></span>
<span data-ttu-id="3c598-130">Anger namnet på den lagrade åtkomst principen som tas bort av cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3c598-130">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c598-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3c598-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="3c598-132">Anger längden på tids gränsen för en server del av en begäran.</span><span class="sxs-lookup"><span data-stu-id="3c598-132">Specifies the length of the time-out period for the server part of a request.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c598-133">-ShareName</span><span class="sxs-lookup"><span data-stu-id="3c598-133">-ShareName</span></span>
<span data-ttu-id="3c598-134">Anger namnet på den lagrings resurs som den här cmdleten tar bort en princip för.</span><span class="sxs-lookup"><span data-stu-id="3c598-134">Specifies the Storage share name for which this cmdlet removes a policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c598-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3c598-135">-Confirm</span></span>
<span data-ttu-id="3c598-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3c598-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c598-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c598-137">-WhatIf</span></span>
<span data-ttu-id="3c598-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3c598-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c598-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3c598-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c598-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c598-140">CommonParameters</span></span>
<span data-ttu-id="3c598-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c598-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c598-142">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c598-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c598-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3c598-143">INPUTS</span></span>

### <span data-ttu-id="3c598-144">System. String</span><span class="sxs-lookup"><span data-stu-id="3c598-144">System.String</span></span>

### <span data-ttu-id="3c598-145">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3c598-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3c598-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3c598-146">OUTPUTS</span></span>

### <span data-ttu-id="3c598-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3c598-147">System.Boolean</span></span>

## <span data-ttu-id="3c598-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3c598-148">NOTES</span></span>

## <span data-ttu-id="3c598-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3c598-149">RELATED LINKS</span></span>

[<span data-ttu-id="3c598-150">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3c598-150">Get-AzStorageShareStoredAccessPolicy</span></span>](./Get-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="3c598-151">New-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3c598-151">New-AzStorageShareStoredAccessPolicy</span></span>](./New-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="3c598-152">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="3c598-152">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="3c598-153">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3c598-153">Set-AzStorageShareStoredAccessPolicy</span></span>](./Set-AzStorageShareStoredAccessPolicy.md)
