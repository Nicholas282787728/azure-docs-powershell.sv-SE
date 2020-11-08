---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/invoke-Azstorageaccountfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Invoke-AzStorageAccountFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Invoke-AzStorageAccountFailover.md
ms.openlocfilehash: 05399377a679a1bb06216364e17b198397a467f5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259804"
---
# <span data-ttu-id="6956f-101">Invoke-AzStorageAccountFailover</span><span class="sxs-lookup"><span data-stu-id="6956f-101">Invoke-AzStorageAccountFailover</span></span>

## <span data-ttu-id="6956f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6956f-102">SYNOPSIS</span></span>
<span data-ttu-id="6956f-103">Anropar redundans för ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="6956f-103">Invokes failover of a Storage account.</span></span>

## <span data-ttu-id="6956f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6956f-104">SYNTAX</span></span>

### <span data-ttu-id="6956f-105">AccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="6956f-105">AccountName (Default)</span></span>
```
Invoke-AzStorageAccountFailover [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6956f-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="6956f-106">AccountObject</span></span>
```
Invoke-AzStorageAccountFailover -InputObject <PSStorageAccount> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6956f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6956f-107">DESCRIPTION</span></span>
<span data-ttu-id="6956f-108">Anropar redundans för ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="6956f-108">Invokes failover of a Storage account.</span></span> <span data-ttu-id="6956f-109">Begäran om redundans kan utlösas för ett lagrings konto i händelse av tillgänglighets problem.</span><span class="sxs-lookup"><span data-stu-id="6956f-109">Failover request can be triggered for a storage account in case of availability issues.</span></span> <span data-ttu-id="6956f-110">Redundansväxlingen sker från lagrings kontots primära kluster till sekundärt kluster för RA-GRS-konton.</span><span class="sxs-lookup"><span data-stu-id="6956f-110">The failover occurs from the storage account's primary cluster to secondary cluster for RA-GRS accounts.</span></span> <span data-ttu-id="6956f-111">Det sekundära klustret blir primärt efter redundans.</span><span class="sxs-lookup"><span data-stu-id="6956f-111">The secondary cluster will become primary after failover.</span></span>
<span data-ttu-id="6956f-112">Förstå följande konsekvenser för ditt lagrings konto innan du initierar redundans: 1,1.</span><span class="sxs-lookup"><span data-stu-id="6956f-112">Please understand the following impact to your storage account before you initiate the failover: 1.1.</span></span> <span data-ttu-id="6956f-113">Kontrol lera den senaste synkroniseringstid med hjälp av skaffa BLOB service stats statistik ( https://docs.microsoft.com/en-us/rest/api/storageservices/get-blob-service-stats) , Hämta tabell tjänst statistik ( https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.table.cloudtableclient.getservicestats?view=azure-dotnet) och få service statistik https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.queue.cloudqueueclient.getservicestats?view=azure-dotnet) för kö (för ditt konto.</span><span class="sxs-lookup"><span data-stu-id="6956f-113">Please check the Last Sync Time using GET Blob Service Stats (https://docs.microsoft.com/en-us/rest/api/storageservices/get-blob-service-stats), GET Table Service Stats (https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.table.cloudtableclient.getservicestats?view=azure-dotnet) and GET Queue Service Stats (https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.queue.cloudqueueclient.getservicestats?view=azure-dotnet) for your account.</span></span> <span data-ttu-id="6956f-114">Det här är de data du kan förlora om du initierar redundans.</span><span class="sxs-lookup"><span data-stu-id="6956f-114">This is the data you may lose if you initiate the failover.</span></span>
<span data-ttu-id="6956f-115">2. efter redundansväxlingen konverteras din lagrings kontotyp till lokalt redundant lagring (LRS).</span><span class="sxs-lookup"><span data-stu-id="6956f-115">2.After the failover, your storage account type will be converted to locally redundant storage(LRS).</span></span> <span data-ttu-id="6956f-116">Du kan konvertera ditt konto för att använda Geo-redundant lagring (GRS).</span><span class="sxs-lookup"><span data-stu-id="6956f-116">You can convert your account to use geo-redundant storage(GRS).</span></span>
<span data-ttu-id="6956f-117">3. När du sedan aktiverar GRS för ditt lagrings konto replikeras data till den nya sekundära regionen.</span><span class="sxs-lookup"><span data-stu-id="6956f-117">3.Once you re-enable GRS for your storage account, Microsoft will replicate data to your new secondary region.</span></span> <span data-ttu-id="6956f-118">Tiden för replikering beror på mängden data som ska replikeras.</span><span class="sxs-lookup"><span data-stu-id="6956f-118">Replication time is dependent on the amount of data to replicate.</span></span> <span data-ttu-id="6956f-119">Observera att det finns bandbredds avgifter för start sidan.</span><span class="sxs-lookup"><span data-stu-id="6956f-119">Please note that there are bandwidth charges for the bootstrap.</span></span> <span data-ttu-id="6956f-120"> https://azure.microsoft.com/en-us/pricing/details/bandwidth/</span><span class="sxs-lookup"><span data-stu-id="6956f-120">https://azure.microsoft.com/en-us/pricing/details/bandwidth/</span></span>

## <span data-ttu-id="6956f-121">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6956f-121">EXAMPLES</span></span>

### <span data-ttu-id="6956f-122">Exempel 1: aktivera redundans för ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="6956f-122">Example 1: Invoke failover of a Storage account</span></span>
```
PS C:\>$account = Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -IncludeGeoReplicationStats
PS C:\>$account.GeoReplicationStats

Status LastSyncTime
------ ------------
Live   11/13/2018 2:44:22 AM

PS C:\>$job = Invoke-AzStorageAccountFailover -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Force -AsJob
PS C:\>$job | Wait-Job
```

<span data-ttu-id="6956f-123">Det här kommandot kontrol lera den senaste synkroniseringstid-tiden för ett lagrings konto och aktiverar sedan failover för det sekundära klustret blir primärt efter redundans.</span><span class="sxs-lookup"><span data-stu-id="6956f-123">This command check the last sync time of a Storage account then invokes failover of it, the secondary cluster will become primary after failover.</span></span> <span data-ttu-id="6956f-124">Eftersom det tar lång tid att redundansväxla kan du föreslå att köra den i Server delen med-AsJob-parametern och sedan vänta på att jobbet är klart.</span><span class="sxs-lookup"><span data-stu-id="6956f-124">Since failover takes a long time, suggest to run it in the backend with -Asjob parameter, and then wait for the job complete.</span></span>

## <span data-ttu-id="6956f-125">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6956f-125">PARAMETERS</span></span>

### <span data-ttu-id="6956f-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6956f-126">-AsJob</span></span>
<span data-ttu-id="6956f-127">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="6956f-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6956f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6956f-128">-DefaultProfile</span></span>
<span data-ttu-id="6956f-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6956f-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6956f-130">-Force</span><span class="sxs-lookup"><span data-stu-id="6956f-130">-Force</span></span>
<span data-ttu-id="6956f-131">Tvinga fram redundans för kontot</span><span class="sxs-lookup"><span data-stu-id="6956f-131">Force to Failover the Account</span></span>

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

### <span data-ttu-id="6956f-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6956f-132">-InputObject</span></span>
<span data-ttu-id="6956f-133">Lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="6956f-133">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6956f-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="6956f-134">-Name</span></span>
<span data-ttu-id="6956f-135">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="6956f-135">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6956f-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6956f-136">-ResourceGroupName</span></span>
<span data-ttu-id="6956f-137">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="6956f-137">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6956f-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6956f-138">-Confirm</span></span>
<span data-ttu-id="6956f-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6956f-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6956f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6956f-140">-WhatIf</span></span>
<span data-ttu-id="6956f-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6956f-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6956f-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6956f-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6956f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6956f-143">CommonParameters</span></span>
<span data-ttu-id="6956f-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6956f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6956f-145">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6956f-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6956f-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6956f-146">INPUTS</span></span>

### <span data-ttu-id="6956f-147">System. String</span><span class="sxs-lookup"><span data-stu-id="6956f-147">System.String</span></span>

## <span data-ttu-id="6956f-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6956f-148">OUTPUTS</span></span>

### <span data-ttu-id="6956f-149">Microsoft. Azure. commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6956f-149">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="6956f-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6956f-150">NOTES</span></span>

## <span data-ttu-id="6956f-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6956f-151">RELATED LINKS</span></span>
