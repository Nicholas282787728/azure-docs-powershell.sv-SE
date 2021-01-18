---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D077DB50-12BC-45AB-8EAC-57810DA83035
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchremotedesktopprotocolfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteDesktopProtocolFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteDesktopProtocolFile.md
ms.openlocfilehash: 3e1b4ce662e7a904fcfb8d4b938f7fe5bbef0f7e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524780"
---
# <span data-ttu-id="7160a-101">Get-AzBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="7160a-101">Get-AzBatchRemoteDesktopProtocolFile</span></span>

## <span data-ttu-id="7160a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7160a-102">SYNOPSIS</span></span>
<span data-ttu-id="7160a-103">Hämtar en RDP-fil från en datornod.</span><span class="sxs-lookup"><span data-stu-id="7160a-103">Gets an RDP file from a compute node.</span></span>

## <span data-ttu-id="7160a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7160a-104">SYNTAX</span></span>

### <span data-ttu-id="7160a-105">Id_Path (standard)</span><span class="sxs-lookup"><span data-stu-id="7160a-105">Id_Path (Default)</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String> -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7160a-106">Id_Stream</span><span class="sxs-lookup"><span data-stu-id="7160a-106">Id_Stream</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String> -DestinationStream <Stream>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7160a-107">InputObject_Path</span><span class="sxs-lookup"><span data-stu-id="7160a-107">InputObject_Path</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7160a-108">InputObject_Stream</span><span class="sxs-lookup"><span data-stu-id="7160a-108">InputObject_Stream</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationStream <Stream>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7160a-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7160a-109">DESCRIPTION</span></span>
<span data-ttu-id="7160a-110">Cmdleten **Get-AzBatchRemoteDesktopProtocolFile** hämtar en RDP-fil (Remote Desktop Protocol) från en datornod och sparar den som en fil eller till en användare som har den här strömmen.</span><span class="sxs-lookup"><span data-stu-id="7160a-110">The **Get-AzBatchRemoteDesktopProtocolFile** cmdlet gets a Remote Desktop Protocol (RDP) file from a compute node and saves it as a file or to a user supplied stream.</span></span>

## <span data-ttu-id="7160a-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7160a-111">EXAMPLES</span></span>

### <span data-ttu-id="7160a-112">Exempel 1: Hämta en RDP-fil från en angiven datornod och spara filen</span><span class="sxs-lookup"><span data-stu-id="7160a-112">Example 1: Get an RDP file from a specified compute node and save the file</span></span>
```
PS C:\>Get-AzBatchRemoteDesktopProtocolFile -PoolId "Pool06" -ComputeNodeId "ComputeNode01" -DestinationPath "C:\PowerShell\ComputeNode01.rdp" -BatchContext $Context
```

<span data-ttu-id="7160a-113">Det här kommandot får en RDP-fil från Compute-noden som har ID-ComputeNode01 i poolen som har ID Pool06.</span><span class="sxs-lookup"><span data-stu-id="7160a-113">This command gets an RDP file from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="7160a-114">Kommandot sparar. RDP-filen som C:\PowerShell\MyComputeNode.rdp.</span><span class="sxs-lookup"><span data-stu-id="7160a-114">The command saves the .rdp file as C:\PowerShell\MyComputeNode.rdp.</span></span>
<span data-ttu-id="7160a-115">Använd Get-AzBatchAccountKey cmdlet för att koppla en kontext till $Context variabeln.</span><span class="sxs-lookup"><span data-stu-id="7160a-115">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="7160a-116">Exempel 2: Hämta en RDP-fil från en datornod och spara filen med pipelinen</span><span class="sxs-lookup"><span data-stu-id="7160a-116">Example 2: Get an RDP file from a compute node and save the file by using the pipeline</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool06" -Id "ComputeNode02" -BatchContext $Context | Get-AzBatchRemoteDesktopProtocolFile -DestinationPath "C:\PowerShell\MyComputeNode02.rdp" -BatchContext $Context
```

<span data-ttu-id="7160a-117">Det här kommandot får Compute-noden med ID-ComputeNode02 i poolen som har ID Pool06.</span><span class="sxs-lookup"><span data-stu-id="7160a-117">This command gets the compute node that has the ID ComputeNode02 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="7160a-118">Kommandot skickar den beräknade noden till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="7160a-118">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7160a-119">Den aktuella cmdleten hämtar en. RPD-fil från noden Compute och sparar sedan innehållet som en fil med namnet C:\PowerShell\MyComputeNode02.rdp.</span><span class="sxs-lookup"><span data-stu-id="7160a-119">The current cmdlet gets an .rpd file from the compute node, and then saves the contents as a file that is named C:\PowerShell\MyComputeNode02.rdp.</span></span>

### <span data-ttu-id="7160a-120">Exempel 3: Hämta en RDP-fil från en angiven datornod och dirigera den till en ström</span><span class="sxs-lookup"><span data-stu-id="7160a-120">Example 3: Get a RDP file from a specified compute node and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchRemoteDesktopProtocolFile "Pool06" -ComputeNodeId "ComputeNode03" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="7160a-121">Det första kommandot skapar en ström genom att använda New-Object cmdlet och lagrar den i $Stream-variabeln.</span><span class="sxs-lookup"><span data-stu-id="7160a-121">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>
<span data-ttu-id="7160a-122">Det andra kommandot får en. RDP-fil från Compute-noden som har ID-ComputeNode03 i poolen som har ID Pool06.</span><span class="sxs-lookup"><span data-stu-id="7160a-122">The second command gets an .rdp file from the compute node that has the ID ComputeNode03 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="7160a-123">Kommandot dirigerar fil innehåll till strömmen i $Stream.</span><span class="sxs-lookup"><span data-stu-id="7160a-123">The command directs file contents to the stream in $Stream.</span></span>

## <span data-ttu-id="7160a-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7160a-124">PARAMETERS</span></span>

### <span data-ttu-id="7160a-125">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="7160a-125">-BatchContext</span></span>
<span data-ttu-id="7160a-126">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="7160a-126">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="7160a-127">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="7160a-127">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="7160a-128">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKey cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="7160a-128">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="7160a-129">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="7160a-129">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="7160a-130">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="7160a-130">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="7160a-131">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="7160a-131">-ComputeNode</span></span>
<span data-ttu-id="7160a-132">Anger en datornod som ett **PSComputeNode** -objekt där. RDP-filen pekar.</span><span class="sxs-lookup"><span data-stu-id="7160a-132">Specifies a compute node, as a **PSComputeNode** object, to which the .rdp file points.</span></span>
<span data-ttu-id="7160a-133">Använd cmdleten Get-AzBatchComputeNode för att hämta ett Compute Node-objekt.</span><span class="sxs-lookup"><span data-stu-id="7160a-133">To obtain a compute node object, use the Get-AzBatchComputeNode cmdlet.</span></span>

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

### <span data-ttu-id="7160a-134">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="7160a-134">-ComputeNodeId</span></span>
<span data-ttu-id="7160a-135">Anger ID för den datornod som. RDP-filen pekar på.</span><span class="sxs-lookup"><span data-stu-id="7160a-135">Specifies the ID of the compute node to which the .rdp file points.</span></span>

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

### <span data-ttu-id="7160a-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7160a-136">-DefaultProfile</span></span>
<span data-ttu-id="7160a-137">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7160a-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7160a-138">-DestinationPath</span><span class="sxs-lookup"><span data-stu-id="7160a-138">-DestinationPath</span></span>
<span data-ttu-id="7160a-139">Anger sökvägen där denna cmdlet sparar. RDP-filen.</span><span class="sxs-lookup"><span data-stu-id="7160a-139">Specifies the file path where this cmdlet saves the .rdp file.</span></span>

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

### <span data-ttu-id="7160a-140">-DestinationStream</span><span class="sxs-lookup"><span data-stu-id="7160a-140">-DestinationStream</span></span>
<span data-ttu-id="7160a-141">Anger den ström där denna cmdlet dirigerar RDP-data.</span><span class="sxs-lookup"><span data-stu-id="7160a-141">Specifies the stream into which this cmdlet directs the RDP data.</span></span>
<span data-ttu-id="7160a-142">Denna cmdlet stänger inte eller spolar inte tillbaka strömmen.</span><span class="sxs-lookup"><span data-stu-id="7160a-142">This cmdlet does not close or rewind this stream.</span></span>

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

### <span data-ttu-id="7160a-143">-PoolId</span><span class="sxs-lookup"><span data-stu-id="7160a-143">-PoolId</span></span>
<span data-ttu-id="7160a-144">Anger ID för poolen som innehåller den datornod som den här cmdleten har en. RDP-fil från.</span><span class="sxs-lookup"><span data-stu-id="7160a-144">Specifies the ID of the pool that contains the compute node from which this cmdlet gets an .rdp file.</span></span>

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

### <span data-ttu-id="7160a-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7160a-145">CommonParameters</span></span>
<span data-ttu-id="7160a-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7160a-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7160a-147">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7160a-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7160a-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7160a-148">INPUTS</span></span>

### <span data-ttu-id="7160a-149">System. String</span><span class="sxs-lookup"><span data-stu-id="7160a-149">System.String</span></span>

### <span data-ttu-id="7160a-150">Microsoft.Azure.Commands.BatCH. Modeller. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="7160a-150">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="7160a-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="7160a-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="7160a-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7160a-152">OUTPUTS</span></span>

### <span data-ttu-id="7160a-153">System. Void</span><span class="sxs-lookup"><span data-stu-id="7160a-153">System.Void</span></span>

## <span data-ttu-id="7160a-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7160a-154">NOTES</span></span>

## <span data-ttu-id="7160a-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7160a-155">RELATED LINKS</span></span>

[<span data-ttu-id="7160a-156">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="7160a-156">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="7160a-157">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="7160a-157">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="7160a-158">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="7160a-158">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
