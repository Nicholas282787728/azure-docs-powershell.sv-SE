---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D077DB50-12BC-45AB-8EAC-57810DA83035
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchremotedesktopprotocolfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteDesktopProtocolFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteDesktopProtocolFile.md
ms.openlocfilehash: 2a147e00dba480a483b10843b17347145a1dc2a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574428"
---
# <span data-ttu-id="7e2db-101">Get-AzureBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="7e2db-101">Get-AzureBatchRemoteDesktopProtocolFile</span></span>

## <span data-ttu-id="7e2db-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7e2db-102">SYNOPSIS</span></span>
<span data-ttu-id="7e2db-103">Hämtar en RDP-fil från en datornod.</span><span class="sxs-lookup"><span data-stu-id="7e2db-103">Gets an RDP file from a compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e2db-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7e2db-104">SYNTAX</span></span>

### <span data-ttu-id="7e2db-105">Id_Path (standard)</span><span class="sxs-lookup"><span data-stu-id="7e2db-105">Id_Path (Default)</span></span>
```
Get-AzureBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String> -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e2db-106">Id_Stream</span><span class="sxs-lookup"><span data-stu-id="7e2db-106">Id_Stream</span></span>
```
Get-AzureBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String>
 -DestinationStream <Stream> -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7e2db-107">InputObject_Path</span><span class="sxs-lookup"><span data-stu-id="7e2db-107">InputObject_Path</span></span>
```
Get-AzureBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e2db-108">InputObject_Stream</span><span class="sxs-lookup"><span data-stu-id="7e2db-108">InputObject_Stream</span></span>
```
Get-AzureBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationStream <Stream>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e2db-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7e2db-109">DESCRIPTION</span></span>
<span data-ttu-id="7e2db-110">Cmdleten **Get-AzureBatchRemoteDesktopProtocolFile** hämtar en RDP-fil (Remote Desktop Protocol) från en datornod och sparar den som en fil eller till en användare som har den här strömmen.</span><span class="sxs-lookup"><span data-stu-id="7e2db-110">The **Get-AzureBatchRemoteDesktopProtocolFile** cmdlet gets a Remote Desktop Protocol (RDP) file from a compute node and saves it as a file or to a user supplied stream.</span></span>

## <span data-ttu-id="7e2db-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7e2db-111">EXAMPLES</span></span>

### <span data-ttu-id="7e2db-112">Exempel 1: Hämta en RDP-fil från en angiven datornod och spara filen</span><span class="sxs-lookup"><span data-stu-id="7e2db-112">Example 1: Get an RDP file from a specified compute node and save the file</span></span>
```
PS C:\>Get-AzureBatchRemoteDesktopProtocolFile -PoolId "Pool06" -ComputeNodeId "ComputeNode01" -DestinationPath "C:\PowerShell\ComputeNode01.rdp" -BatchContext $Context
```

<span data-ttu-id="7e2db-113">Det här kommandot får en RDP-fil från Compute-noden som har ID-ComputeNode01 i poolen som har ID Pool06.</span><span class="sxs-lookup"><span data-stu-id="7e2db-113">This command gets an RDP file from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="7e2db-114">Kommandot sparar. RDP-filen som C:\PowerShell\MyComputeNode.rdp.</span><span class="sxs-lookup"><span data-stu-id="7e2db-114">The command saves the .rdp file as C:\PowerShell\MyComputeNode.rdp.</span></span>
<span data-ttu-id="7e2db-115">Använd Get-AzureRmBatchAccountKeys cmdlet för att koppla en kontext till $Context variabeln.</span><span class="sxs-lookup"><span data-stu-id="7e2db-115">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="7e2db-116">Exempel 2: Hämta en RDP-fil från en datornod och spara filen med pipelinen</span><span class="sxs-lookup"><span data-stu-id="7e2db-116">Example 2: Get an RDP file from a compute node and save the file by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "Pool06" -Id "ComputeNode02" -BatchContext $Context | Get-AzureBatchRemoteDesktopProtocolFile -DestinationPath "C:\PowerShell\MyComputeNode02.rdp" -BatchContext $Context
```

<span data-ttu-id="7e2db-117">Det här kommandot får Compute-noden med ID-ComputeNode02 i poolen som har ID Pool06.</span><span class="sxs-lookup"><span data-stu-id="7e2db-117">This command gets the compute node that has the ID ComputeNode02 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="7e2db-118">Kommandot skickar den beräknade noden till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="7e2db-118">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7e2db-119">Den aktuella cmdleten hämtar en. RPD-fil från noden Compute och sparar sedan innehållet som en fil med namnet C:\PowerShell\MyComputeNode02.rdp.</span><span class="sxs-lookup"><span data-stu-id="7e2db-119">The current cmdlet gets an .rpd file from the compute node, and then saves the contents as a file that is named C:\PowerShell\MyComputeNode02.rdp.</span></span>

### <span data-ttu-id="7e2db-120">Exempel 3: Hämta en RDP-fil från en angiven datornod och dirigera den till en ström</span><span class="sxs-lookup"><span data-stu-id="7e2db-120">Example 3: Get a RDP file from a specified compute node and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzureBatchRemoteDesktopProtocolFile "Pool06" -ComputeNodeId "ComputeNode03" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="7e2db-121">Det första kommandot skapar en ström genom att använda New-Object cmdlet och lagrar den i $Stream-variabeln.</span><span class="sxs-lookup"><span data-stu-id="7e2db-121">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>

<span data-ttu-id="7e2db-122">Det andra kommandot får en. RDP-fil från Compute-noden som har ID-ComputeNode03 i poolen som har ID Pool06.</span><span class="sxs-lookup"><span data-stu-id="7e2db-122">The second command gets an .rdp file from the compute node that has the ID ComputeNode03 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="7e2db-123">Kommandot dirigerar fil innehåll till strömmen i $Stream.</span><span class="sxs-lookup"><span data-stu-id="7e2db-123">The command directs file contents to the stream in $Stream.</span></span>

## <span data-ttu-id="7e2db-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7e2db-124">PARAMETERS</span></span>

### <span data-ttu-id="7e2db-125">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="7e2db-125">-BatchContext</span></span>
<span data-ttu-id="7e2db-126">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="7e2db-126">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="7e2db-127">Om du använder Get-AzureRmBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="7e2db-127">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="7e2db-128">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="7e2db-128">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="7e2db-129">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="7e2db-129">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="7e2db-130">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="7e2db-130">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e2db-131">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="7e2db-131">-ComputeNode</span></span>
<span data-ttu-id="7e2db-132">Anger en datornod som ett **PSComputeNode** -objekt där. RDP-filen pekar.</span><span class="sxs-lookup"><span data-stu-id="7e2db-132">Specifies a compute node, as a **PSComputeNode** object, to which the .rdp file points.</span></span>
<span data-ttu-id="7e2db-133">Använd cmdleten Get-AzureBatchComputeNode för att hämta ett Compute Node-objekt.</span><span class="sxs-lookup"><span data-stu-id="7e2db-133">To obtain a compute node object, use the Get-AzureBatchComputeNode cmdlet.</span></span>

```yaml
Type: PSComputeNode
Parameter Sets: InputObject_Path, InputObject_Stream
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e2db-134">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="7e2db-134">-ComputeNodeId</span></span>
<span data-ttu-id="7e2db-135">Anger ID för den datornod som. RDP-filen pekar på.</span><span class="sxs-lookup"><span data-stu-id="7e2db-135">Specifies the ID of the compute node to which the .rdp file points.</span></span>

```yaml
Type: String
Parameter Sets: Id_Path, Id_Stream
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e2db-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e2db-136">-DefaultProfile</span></span>
<span data-ttu-id="7e2db-137">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7e2db-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e2db-138">-DestinationPath</span><span class="sxs-lookup"><span data-stu-id="7e2db-138">-DestinationPath</span></span>
<span data-ttu-id="7e2db-139">Anger sökvägen där denna cmdlet sparar. RDP-filen.</span><span class="sxs-lookup"><span data-stu-id="7e2db-139">Specifies the file path where this cmdlet saves the .rdp file.</span></span>

```yaml
Type: String
Parameter Sets: Id_Path, InputObject_Path
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e2db-140">-DestinationStream</span><span class="sxs-lookup"><span data-stu-id="7e2db-140">-DestinationStream</span></span>
<span data-ttu-id="7e2db-141">Anger den ström där denna cmdlet dirigerar RDP-data.</span><span class="sxs-lookup"><span data-stu-id="7e2db-141">Specifies the stream into which this cmdlet directs the RDP data.</span></span>
<span data-ttu-id="7e2db-142">Denna cmdlet stänger inte eller spolar inte tillbaka strömmen.</span><span class="sxs-lookup"><span data-stu-id="7e2db-142">This cmdlet does not close or rewind this stream.</span></span>

```yaml
Type: Stream
Parameter Sets: Id_Stream, InputObject_Stream
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e2db-143">-PoolId</span><span class="sxs-lookup"><span data-stu-id="7e2db-143">-PoolId</span></span>
<span data-ttu-id="7e2db-144">Anger ID för poolen som innehåller den datornod som den här cmdleten har en. RDP-fil från.</span><span class="sxs-lookup"><span data-stu-id="7e2db-144">Specifies the ID of the pool that contains the compute node from which this cmdlet gets an .rdp file.</span></span>

```yaml
Type: String
Parameter Sets: Id_Path, Id_Stream
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e2db-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e2db-145">CommonParameters</span></span>
<span data-ttu-id="7e2db-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e2db-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e2db-147">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e2db-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e2db-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7e2db-148">INPUTS</span></span>

### <span data-ttu-id="7e2db-149">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="7e2db-149">BatchAccountContext</span></span>
<span data-ttu-id="7e2db-150">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="7e2db-150">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="7e2db-151">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="7e2db-151">PSComputeNode</span></span>
<span data-ttu-id="7e2db-152">Parametern ' ComputeNode ' godkänner värdet av typen ' PSComputeNode ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="7e2db-152">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="7e2db-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7e2db-153">OUTPUTS</span></span>

## <span data-ttu-id="7e2db-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7e2db-154">NOTES</span></span>

## <span data-ttu-id="7e2db-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7e2db-155">RELATED LINKS</span></span>

[<span data-ttu-id="7e2db-156">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="7e2db-156">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="7e2db-157">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="7e2db-157">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="7e2db-158">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="7e2db-158">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


