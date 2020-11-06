---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D077DB50-12BC-45AB-8EAC-57810DA83035
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteDesktopProtocolFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteDesktopProtocolFile.md
ms.openlocfilehash: 37d91dc6fd9d90291c7b619fdb9839d6d9af83b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586243"
---
# <span data-ttu-id="90508-101">Get-AzureBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="90508-101">Get-AzureBatchRemoteDesktopProtocolFile</span></span>

## <span data-ttu-id="90508-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="90508-102">SYNOPSIS</span></span>
<span data-ttu-id="90508-103">Hämtar en RDP-fil från en datornod.</span><span class="sxs-lookup"><span data-stu-id="90508-103">Gets an RDP file from a compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90508-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="90508-104">SYNTAX</span></span>

### <span data-ttu-id="90508-105">Id_Path (standard)</span><span class="sxs-lookup"><span data-stu-id="90508-105">Id_Path (Default)</span></span>
```
Get-AzureBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String> -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90508-106">Id_Stream</span><span class="sxs-lookup"><span data-stu-id="90508-106">Id_Stream</span></span>
```
Get-AzureBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String>
 -DestinationStream <Stream> -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="90508-107">InputObject_Path</span><span class="sxs-lookup"><span data-stu-id="90508-107">InputObject_Path</span></span>
```
Get-AzureBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90508-108">InputObject_Stream</span><span class="sxs-lookup"><span data-stu-id="90508-108">InputObject_Stream</span></span>
```
Get-AzureBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationStream <Stream>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90508-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="90508-109">DESCRIPTION</span></span>
<span data-ttu-id="90508-110">Cmdleten **Get-AzureBatchRemoteDesktopProtocolFile** hämtar en RDP-fil (Remote Desktop Protocol) från en datornod och sparar den som en fil eller till en användare som har den här strömmen.</span><span class="sxs-lookup"><span data-stu-id="90508-110">The **Get-AzureBatchRemoteDesktopProtocolFile** cmdlet gets a Remote Desktop Protocol (RDP) file from a compute node and saves it as a file or to a user supplied stream.</span></span>

## <span data-ttu-id="90508-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="90508-111">EXAMPLES</span></span>

### <span data-ttu-id="90508-112">Exempel 1: Hämta en RDP-fil från en angiven datornod och spara filen</span><span class="sxs-lookup"><span data-stu-id="90508-112">Example 1: Get an RDP file from a specified compute node and save the file</span></span>
```
PS C:\>Get-AzureBatchRemoteDesktopProtocolFile -PoolId "Pool06" -ComputeNodeId "ComputeNode01" -DestinationPath "C:\PowerShell\ComputeNode01.rdp" -BatchContext $Context
```

<span data-ttu-id="90508-113">Det här kommandot får en RDP-fil från Compute-noden som har ID-ComputeNode01 i poolen som har ID Pool06.</span><span class="sxs-lookup"><span data-stu-id="90508-113">This command gets an RDP file from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="90508-114">Kommandot sparar. RDP-filen som C:\PowerShell\MyComputeNode.rdp.</span><span class="sxs-lookup"><span data-stu-id="90508-114">The command saves the .rdp file as C:\PowerShell\MyComputeNode.rdp.</span></span>
<span data-ttu-id="90508-115">Använd Get-AzureRmBatchAccountKeys cmdlet för att koppla en kontext till $Context variabeln.</span><span class="sxs-lookup"><span data-stu-id="90508-115">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="90508-116">Exempel 2: Hämta en RDP-fil från en datornod och spara filen med pipelinen</span><span class="sxs-lookup"><span data-stu-id="90508-116">Example 2: Get an RDP file from a compute node and save the file by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "Pool06" -Id "ComputeNode02" -BatchContext $Context | Get-AzureBatchRemoteDesktopProtocolFile -DestinationPath "C:\PowerShell\MyComputeNode02.rdp" -BatchContext $Context
```

<span data-ttu-id="90508-117">Det här kommandot får Compute-noden med ID-ComputeNode02 i poolen som har ID Pool06.</span><span class="sxs-lookup"><span data-stu-id="90508-117">This command gets the compute node that has the ID ComputeNode02 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="90508-118">Kommandot skickar den beräknade noden till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="90508-118">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="90508-119">Den aktuella cmdleten hämtar en. RPD-fil från noden Compute och sparar sedan innehållet som en fil med namnet C:\PowerShell\MyComputeNode02.rdp.</span><span class="sxs-lookup"><span data-stu-id="90508-119">The current cmdlet gets an .rpd file from the compute node, and then saves the contents as a file that is named C:\PowerShell\MyComputeNode02.rdp.</span></span>

### <span data-ttu-id="90508-120">Exempel 3: Hämta en RDP-fil från en angiven datornod och dirigera den till en ström</span><span class="sxs-lookup"><span data-stu-id="90508-120">Example 3: Get a RDP file from a specified compute node and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzureBatchRemoteDesktopProtocolFile "Pool06" -ComputeNodeId "ComputeNode03" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="90508-121">Det första kommandot skapar en ström genom att använda New-Object cmdlet och lagrar den i $Stream-variabeln.</span><span class="sxs-lookup"><span data-stu-id="90508-121">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>

<span data-ttu-id="90508-122">Det andra kommandot får en. RDP-fil från Compute-noden som har ID-ComputeNode03 i poolen som har ID Pool06.</span><span class="sxs-lookup"><span data-stu-id="90508-122">The second command gets an .rdp file from the compute node that has the ID ComputeNode03 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="90508-123">Kommandot dirigerar fil innehåll till strömmen i $Stream.</span><span class="sxs-lookup"><span data-stu-id="90508-123">The command directs file contents to the stream in $Stream.</span></span>

## <span data-ttu-id="90508-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="90508-124">PARAMETERS</span></span>

### <span data-ttu-id="90508-125">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="90508-125">-BatchContext</span></span>
<span data-ttu-id="90508-126">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="90508-126">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="90508-127">Använd Get-AzureRmBatchAccountKeys cmdlet för att få ett **BatchAccountContext** -objekt som innehåller åtkomst nycklar för prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="90508-127">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90508-128">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="90508-128">-ComputeNode</span></span>
<span data-ttu-id="90508-129">Anger en datornod som ett **PSComputeNode** -objekt där. RDP-filen pekar.</span><span class="sxs-lookup"><span data-stu-id="90508-129">Specifies a compute node, as a **PSComputeNode** object, to which the .rdp file points.</span></span>
<span data-ttu-id="90508-130">Använd cmdleten Get-AzureBatchComputeNode för att hämta ett Compute Node-objekt.</span><span class="sxs-lookup"><span data-stu-id="90508-130">To obtain a compute node object, use the Get-AzureBatchComputeNode cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: InputObject_Path, InputObject_Stream
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90508-131">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="90508-131">-ComputeNodeId</span></span>
<span data-ttu-id="90508-132">Anger ID för den datornod som. RDP-filen pekar på.</span><span class="sxs-lookup"><span data-stu-id="90508-132">Specifies the ID of the compute node to which the .rdp file points.</span></span>

```yaml
Type: System.String
Parameter Sets: Id_Path, Id_Stream
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90508-133">-DestinationPath</span><span class="sxs-lookup"><span data-stu-id="90508-133">-DestinationPath</span></span>
<span data-ttu-id="90508-134">Anger sökvägen där denna cmdlet sparar. RDP-filen.</span><span class="sxs-lookup"><span data-stu-id="90508-134">Specifies the file path where this cmdlet saves the .rdp file.</span></span>

```yaml
Type: System.String
Parameter Sets: Id_Path, InputObject_Path
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90508-135">-DestinationStream</span><span class="sxs-lookup"><span data-stu-id="90508-135">-DestinationStream</span></span>
<span data-ttu-id="90508-136">Anger den ström där denna cmdlet dirigerar RDP-data.</span><span class="sxs-lookup"><span data-stu-id="90508-136">Specifies the stream into which this cmdlet directs the RDP data.</span></span>
<span data-ttu-id="90508-137">Denna cmdlet stänger inte eller spolar inte tillbaka strömmen.</span><span class="sxs-lookup"><span data-stu-id="90508-137">This cmdlet does not close or rewind this stream.</span></span>

```yaml
Type: System.IO.Stream
Parameter Sets: Id_Stream, InputObject_Stream
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90508-138">-PoolId</span><span class="sxs-lookup"><span data-stu-id="90508-138">-PoolId</span></span>
<span data-ttu-id="90508-139">Anger ID för poolen som innehåller den datornod som den här cmdleten har en. RDP-fil från.</span><span class="sxs-lookup"><span data-stu-id="90508-139">Specifies the ID of the pool that contains the compute node from which this cmdlet gets an .rdp file.</span></span>

```yaml
Type: System.String
Parameter Sets: Id_Path, Id_Stream
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90508-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90508-140">-DefaultProfile</span></span>
<span data-ttu-id="90508-141">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="90508-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90508-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90508-142">CommonParameters</span></span>
<span data-ttu-id="90508-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90508-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90508-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90508-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90508-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="90508-145">INPUTS</span></span>

### <span data-ttu-id="90508-146">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="90508-146">BatchAccountContext</span></span>
<span data-ttu-id="90508-147">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="90508-147">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="90508-148">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="90508-148">PSComputeNode</span></span>
<span data-ttu-id="90508-149">Parametern ' ComputeNode ' godkänner värdet av typen ' PSComputeNode ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="90508-149">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="90508-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="90508-150">OUTPUTS</span></span>

## <span data-ttu-id="90508-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="90508-151">NOTES</span></span>

## <span data-ttu-id="90508-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="90508-152">RELATED LINKS</span></span>

[<span data-ttu-id="90508-153">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="90508-153">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="90508-154">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="90508-154">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="90508-155">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="90508-155">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


