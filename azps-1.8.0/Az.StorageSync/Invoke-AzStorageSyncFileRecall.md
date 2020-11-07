---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/invoke-Azstoragesyncfilerecall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncFileRecall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncFileRecall.md
ms.openlocfilehash: 5463c20274f60c2d6fb6c4807bf2c4d27da76808
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746219"
---
# <span data-ttu-id="3ed89-101">Invoke-AzStorageSyncFileRecall</span><span class="sxs-lookup"><span data-stu-id="3ed89-101">Invoke-AzStorageSyncFileRecall</span></span>

## <span data-ttu-id="3ed89-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3ed89-102">SYNOPSIS</span></span>
<span data-ttu-id="3ed89-103">Det här kommandot återställer alla nivåbaserade filer tillbaka till lokala diskar.</span><span class="sxs-lookup"><span data-stu-id="3ed89-103">This command recalls all tiered files back to local disk.</span></span>

## <span data-ttu-id="3ed89-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3ed89-104">SYNTAX</span></span>

### <span data-ttu-id="3ed89-105">ObjectParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="3ed89-105">ObjectParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncFileRecall [-InputObject] <PSServerEndpoint> [-Pattern <String>] [-RecallPath <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ed89-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ed89-106">StringParameterSet</span></span>
```
Invoke-AzStorageSyncFileRecall [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Pattern <String>] [-RecallPath <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ed89-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ed89-107">ResourceIdParameterSet</span></span>
```
Invoke-AzStorageSyncFileRecall [-ResourceId] <String> [-Pattern <String>] [-RecallPath <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ed89-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3ed89-108">DESCRIPTION</span></span>
<span data-ttu-id="3ed89-109">När moln lager är aktiverat på en server slut punkt (en specifik plats på en registrerad Server) kan det här kommandot användas för att återkalla alla nivåbaserade filer till lokala diskar.</span><span class="sxs-lookup"><span data-stu-id="3ed89-109">When cloud tiering is enabled on a server endpoint (a specific location on a registered server) then this command can be used to recall all tiered files to local disk.</span></span> <span data-ttu-id="3ed89-110">Vi rekommenderar starkt att du inaktiverar moln skiktning på den här server slut punkten innan du påbörjar återställningen.</span><span class="sxs-lookup"><span data-stu-id="3ed89-110">It is highly recommended to disable cloud tiering on this server endpoint before starting recall.</span></span> <span data-ttu-id="3ed89-111">Om du fortfarande har en lager nivå kan du komma ihåg att återkalla andra filer som missar för att uppfylla allt innehåll som finns på lokala diskar.</span><span class="sxs-lookup"><span data-stu-id="3ed89-111">If tiering is still on, recall might lead to other files getting tiered which misses to achieve the desired goal of all content residing on local disk.</span></span>

## <span data-ttu-id="3ed89-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3ed89-112">EXAMPLES</span></span>

### <span data-ttu-id="3ed89-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3ed89-113">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncFileRecall -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -ServerEndpointName "myServerEndpointName"
```

<span data-ttu-id="3ed89-114">Detta kommando återkallar rekursivt alla skiktade filer under rot Sök vägen för den angivna Server slut punkten.</span><span class="sxs-lookup"><span data-stu-id="3ed89-114">This command recursively recalls all tiered files located under the root path of the specified server endpoint.</span></span>

## <span data-ttu-id="3ed89-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3ed89-115">PARAMETERS</span></span>

### <span data-ttu-id="3ed89-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3ed89-116">-AsJob</span></span>
<span data-ttu-id="3ed89-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="3ed89-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3ed89-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ed89-118">-DefaultProfile</span></span>
<span data-ttu-id="3ed89-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3ed89-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ed89-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ed89-120">-InputObject</span></span>
<span data-ttu-id="3ed89-121">SyncGroup-objekt som normalt passerar genom parametern.</span><span class="sxs-lookup"><span data-stu-id="3ed89-121">SyncGroup Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint
Parameter Sets: ObjectParameterSet
Aliases: RegisteredServer

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ed89-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="3ed89-122">-Name</span></span>
<span data-ttu-id="3ed89-123">Namn på ServerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="3ed89-123">Name of the ServerEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ServerEndpointName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ed89-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3ed89-124">-PassThru</span></span>
<span data-ttu-id="3ed89-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="3ed89-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="3ed89-126">-Mönster</span><span class="sxs-lookup"><span data-stu-id="3ed89-126">-Pattern</span></span>
<span data-ttu-id="3ed89-127">Mönster för fil namnet</span><span class="sxs-lookup"><span data-stu-id="3ed89-127">Pattern of the file name</span></span>

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

### <span data-ttu-id="3ed89-128">-RecallPath</span><span class="sxs-lookup"><span data-stu-id="3ed89-128">-RecallPath</span></span>
<span data-ttu-id="3ed89-129">Sökväg som måste återkallas.</span><span class="sxs-lookup"><span data-stu-id="3ed89-129">Recall path which need to be recalled.</span></span>

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

### <span data-ttu-id="3ed89-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ed89-130">-ResourceGroupName</span></span>
<span data-ttu-id="3ed89-131">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="3ed89-131">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ed89-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ed89-132">-ResourceId</span></span>
<span data-ttu-id="3ed89-133">Resurs-ID för ServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3ed89-133">ServerEndpoint Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ed89-134">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="3ed89-134">-StorageSyncServiceName</span></span>
<span data-ttu-id="3ed89-135">Namn på StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="3ed89-135">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ed89-136">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="3ed89-136">-SyncGroupName</span></span>
<span data-ttu-id="3ed89-137">Namn på SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="3ed89-137">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ed89-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ed89-138">CommonParameters</span></span>
<span data-ttu-id="3ed89-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ed89-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ed89-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ed89-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ed89-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3ed89-141">INPUTS</span></span>

### <span data-ttu-id="3ed89-142">System. String</span><span class="sxs-lookup"><span data-stu-id="3ed89-142">System.String</span></span>

### <span data-ttu-id="3ed89-143">Microsoft. Azure. commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3ed89-143">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="3ed89-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3ed89-144">OUTPUTS</span></span>

### <span data-ttu-id="3ed89-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3ed89-145">System.Boolean</span></span>

## <span data-ttu-id="3ed89-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3ed89-146">NOTES</span></span>

## <span data-ttu-id="3ed89-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3ed89-147">RELATED LINKS</span></span>
