---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 5605F11E-EEA0-4C32-8445-2E001D56BC47
online version: ''
schema: 2.0.0
ms.openlocfilehash: e364692858cf190b48b61f4d38fbf483d229ffb7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093246"
---
# <span data-ttu-id="b5809-101">New-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="b5809-101">New-AzureStorSimpleDeviceVolumeContainer</span></span>

## <span data-ttu-id="b5809-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b5809-102">SYNOPSIS</span></span>
<span data-ttu-id="b5809-103">Skapar en volym behållare.</span><span class="sxs-lookup"><span data-stu-id="b5809-103">Creates a volume container.</span></span>

## <span data-ttu-id="b5809-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b5809-104">SYNTAX</span></span>

```
New-AzureStorSimpleDeviceVolumeContainer -DeviceName <String> -VolumeContainerName <String>
 -PrimaryStorageAccountCredential <StorageAccountCredentialResponse> -BandWidthRateInMbps <Int32>
 [-EncryptionEnabled <Boolean>] [-EncryptionKey <String>] [-WaitForComplete] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="b5809-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b5809-105">DESCRIPTION</span></span>
<span data-ttu-id="b5809-106">Cmdleten **New-AzureStorSimpleDeviceVolumeContainer** skapar en volym behållare.</span><span class="sxs-lookup"><span data-stu-id="b5809-106">The **New-AzureStorSimpleDeviceVolumeContainer** cmdlet creates a volume container.</span></span>
<span data-ttu-id="b5809-107">Du måste koppla en autentiseringsuppgift för lagrings konton till den nya volymen.</span><span class="sxs-lookup"><span data-stu-id="b5809-107">You must associate a storage account credential with the new volume container.</span></span>
<span data-ttu-id="b5809-108">Använd cmdleten **Get-AzureStorSimpleStorageAccountCredential** för att erhålla en autentiseringsuppgift för lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="b5809-108">To obtain a storage account credential, use the **Get-AzureStorSimpleStorageAccountCredential** cmdlet.</span></span>

## <span data-ttu-id="b5809-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b5809-109">EXAMPLES</span></span>

### <span data-ttu-id="b5809-110">Exempel 1: skapa en behållare</span><span class="sxs-lookup"><span data-stu-id="b5809-110">Example 1: Create a container</span></span>
```
PS C:\>Get-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoAccount" | New-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "Container08" -BandWidthRateInMbps 256
VERBOSE: ClientRequestId: 96a4ccd4-f2a9-4820-8bc8-e6b7b56dce0d_PS
VERBOSE: ClientRequestId: 90be20db-098a-4f2b-a6da-9da6f533a846_PS
VERBOSE: ClientRequestId: 410fd33a-8fa3-4ae5-a1bf-1b6da9b34ffc_PS
VERBOSE: Storage Access Credential with name ContosoAccount found! 
VERBOSE: ClientRequestId: 0a6d1008-ba1f-43b2-a424-9c86be2fb83b_PS
VERBOSE: ClientRequestId: 08f0d657-a130-4a25-8090-270c58b479dc_PS
VERBOSE: ClientRequestId: 0f3e894a-b031-467c-a258-41b74c89cf18_PS
5b192120-9df0-40ed-b75e-b4e728bd37ef
VERBOSE: The create task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
5b192120-9df0-40ed-b75e-b4e728bd37ef for tracking the task's status
```

<span data-ttu-id="b5809-111">Det här kommandot hämtar autentiseringsuppgifterna för lagrings kontot för kontot som heter ContosoAccount med hjälp av cmdleten **Get-AzureStorSimpleStorageAccountCredential** .</span><span class="sxs-lookup"><span data-stu-id="b5809-111">This command gets the storage account credential for the account named ContosoAccount by using the **Get-AzureStorSimpleStorageAccountCredential** cmdlet.</span></span>
<span data-ttu-id="b5809-112">Kommandot skickar autentiseringsuppgiften till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="b5809-112">The command passes the credential to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b5809-113">Denna cmdlet använder autentiseringsuppgifterna från denna cmdlet för att skapa behållaren med namnet Container08 på enheten som heter Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="b5809-113">This cmdlet uses the credential from that cmdlet to create the container named Container08 on the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="b5809-114">Det här kommandot startar jobbet och returnerar sedan ett **TaskResponse** -objekt.</span><span class="sxs-lookup"><span data-stu-id="b5809-114">This command starts the job, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="b5809-115">Använd cmdleten **Get-AzureStorSimpleTask** för att se status för jobbet.</span><span class="sxs-lookup"><span data-stu-id="b5809-115">To see the status of the job, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

## <span data-ttu-id="b5809-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b5809-116">PARAMETERS</span></span>

### <span data-ttu-id="b5809-117">-BandWidthRateInMbps</span><span class="sxs-lookup"><span data-stu-id="b5809-117">-BandWidthRateInMbps</span></span>
<span data-ttu-id="b5809-118">Anger bandbredds hastigheten i megabit per sekund (Mbps).</span><span class="sxs-lookup"><span data-stu-id="b5809-118">Specifies the bandwidth rate in megabits per second (Mbps).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: CloudBandwidthInMbps

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5809-119">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="b5809-119">-DeviceName</span></span>
<span data-ttu-id="b5809-120">Anger namnet på den StorSimple-enhet där volym behållaren ska skapas.</span><span class="sxs-lookup"><span data-stu-id="b5809-120">Specifies the name of the StorSimple device on which to create the volume container.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5809-121">-EncryptionEnabled</span><span class="sxs-lookup"><span data-stu-id="b5809-121">-EncryptionEnabled</span></span>
<span data-ttu-id="b5809-122">Anger om kryptering ska aktive ras.</span><span class="sxs-lookup"><span data-stu-id="b5809-122">Indicates whether to enable encryption.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5809-123">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="b5809-123">-EncryptionKey</span></span>
<span data-ttu-id="b5809-124">Anger krypterings knappen.</span><span class="sxs-lookup"><span data-stu-id="b5809-124">Specifies the encryption key.</span></span>

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

### <span data-ttu-id="b5809-125">-PrimaryStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="b5809-125">-PrimaryStorageAccountCredential</span></span>
<span data-ttu-id="b5809-126">Anger autentiseringsuppgiften som ett **StorageAccountCredential** -objekt som ska kopplas till den nya volymen.</span><span class="sxs-lookup"><span data-stu-id="b5809-126">Specifies the credential, as a **StorageAccountCredential** object, to associate with the new volume container.</span></span>
<span data-ttu-id="b5809-127">Om du vill hämta ett **StorageAccountCredential** -objekt använder du cmdleten **Get-AzureStorSimpleStorageAccountCredential** .</span><span class="sxs-lookup"><span data-stu-id="b5809-127">To obtain a **StorageAccountCredential** object, use the **Get-AzureStorSimpleStorageAccountCredential** cmdlet.</span></span>

```yaml
Type: StorageAccountCredentialResponse
Parameter Sets: (All)
Aliases: StorageAccount

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5809-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="b5809-128">-Profile</span></span>
<span data-ttu-id="b5809-129">Anger en Azure-profil.</span><span class="sxs-lookup"><span data-stu-id="b5809-129">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5809-130">-VolumeContainerName</span><span class="sxs-lookup"><span data-stu-id="b5809-130">-VolumeContainerName</span></span>
<span data-ttu-id="b5809-131">Anger namnet på den volym behållare som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="b5809-131">Specifies the name of the volume container to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5809-132">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="b5809-132">-WaitForComplete</span></span>
<span data-ttu-id="b5809-133">Anger att denna cmdlet väntar på att åtgärden ska slutföras innan den återfår kontroll till Windows PowerShell-konsolen.</span><span class="sxs-lookup"><span data-stu-id="b5809-133">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="b5809-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5809-134">CommonParameters</span></span>
<span data-ttu-id="b5809-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5809-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5809-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5809-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5809-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b5809-137">INPUTS</span></span>

### <span data-ttu-id="b5809-138">StorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="b5809-138">StorageAccountCredential</span></span>
<span data-ttu-id="b5809-139">Denna cmdlet accepterar ett **PrimaryStorageAccountCredential** -objekt som ska kopplas till volymen.</span><span class="sxs-lookup"><span data-stu-id="b5809-139">This cmdlet accepts a **PrimaryStorageAccountCredential** object to associate with the volume container.</span></span>

## <span data-ttu-id="b5809-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b5809-140">OUTPUTS</span></span>

### <span data-ttu-id="b5809-141">TaskStatusInfo</span><span class="sxs-lookup"><span data-stu-id="b5809-141">TaskStatusInfo</span></span>
<span data-ttu-id="b5809-142">Denna cmdlet returnerar ett **TaskStatusInfo** -objekt om du anger parametern *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="b5809-142">This cmdlet returns a **TaskStatusInfo** object, if you specify the *WaitForComplete* parameter.</span></span>

## <span data-ttu-id="b5809-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b5809-143">NOTES</span></span>

## <span data-ttu-id="b5809-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b5809-144">RELATED LINKS</span></span>

[<span data-ttu-id="b5809-145">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="b5809-145">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="b5809-146">Remove-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="b5809-146">Remove-AzureStorSimpleDeviceVolumeContainer</span></span>](./Remove-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="b5809-147">Get-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="b5809-147">Get-AzureStorSimpleStorageAccountCredential</span></span>](./Get-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="b5809-148">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="b5809-148">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


