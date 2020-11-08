---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: BC68C60C-86E3-4857-95AE-1A915A841F7D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 803bc4006e5be8582183248c22115fcd51862d13
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093243"
---
# <span data-ttu-id="1e7d1-101">New-AzureStorSimpleInlineStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="1e7d1-101">New-AzureStorSimpleInlineStorageAccountCredential</span></span>

## <span data-ttu-id="1e7d1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1e7d1-102">SYNOPSIS</span></span>
<span data-ttu-id="1e7d1-103">Skapar en referens till ett inline Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="1e7d1-103">Creates an inline storage account credential.</span></span>

## <span data-ttu-id="1e7d1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1e7d1-104">SYNTAX</span></span>

```
New-AzureStorSimpleInlineStorageAccountCredential -StorageAccountName <String> -StorageAccountKey <String>
 [-Endpoint <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1e7d1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1e7d1-105">DESCRIPTION</span></span>
<span data-ttu-id="1e7d1-106">**New-AzureStorSimpleInlineStorageAccountCredential** cmdlet skapar ett inline-objekt med behörigheten Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="1e7d1-106">The **New-AzureStorSimpleInlineStorageAccountCredential** cmdlet creates an inline Azure storage account credential object.</span></span>
<span data-ttu-id="1e7d1-107">Den här cmdleten skapar ett objekt för uppgifts uppgifter.</span><span class="sxs-lookup"><span data-stu-id="1e7d1-107">This cmdlet creates a dummy credential object.</span></span>
<span data-ttu-id="1e7d1-108">Du kan använda cmdleten **New-AzureStorSimpleDeviceVolumeContainer** och den aktuella cmdleten i samma kommando genom att använda Windows PowerShell pipeline.</span><span class="sxs-lookup"><span data-stu-id="1e7d1-108">You can use the **New-AzureStorSimpleDeviceVolumeContainer** cmdlet and the current cmdlet in the same command by using the Windows PowerShell pipeline.</span></span>
<span data-ttu-id="1e7d1-109">Den faktiska autentiseringsuppgiften för lagrings kontot skapas som en del av volymen.</span><span class="sxs-lookup"><span data-stu-id="1e7d1-109">The actual storage account credential object is created as part of creation of the volume container.</span></span>

## <span data-ttu-id="1e7d1-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1e7d1-110">EXAMPLES</span></span>

### <span data-ttu-id="1e7d1-111">Exempel 1: skapa en infogad referens till lagrings konto</span><span class="sxs-lookup"><span data-stu-id="1e7d1-111">Example 1: Create a storage account credential inline</span></span>
```
PS C:\>New-AzureStorSimpleInlineStorageAccountCredential -Name "contoso76" -Key x6o/tpZh8Coo8Tteo0NHLksTOKr/P9Vufo0LZNGdPGVTSUu00/p6ta1w9gRbVBNjzN8aa504kH2zkEsfUme+kw== | New-AzureStorSimpleDeviceVolumeContainer -Name "VolumeContainer_06" -DeviceName Contoso_App3 -BandWidthRate 256 -EncryptionEnabled $True -EncryptionKey "Key22" -WaitForComplete
VERBOSE: ClientRequestId: 535d24d5-1ed8-4759-92b2-dd492f94e23e_PS
VERBOSE: ClientRequestId: f32fc069-96c9-4fd9-a71a-0e62d81f25d8_PS
VERBOSE: ClientRequestId: 4376a931-89f5-448f-92bd-b2f7234244c9_PS
VERBOSE: ClientRequestId: 980109d4-7d76-40d0-ae3c-db539e2cb486_PS
VERBOSE: Encryption in progress... 
VERBOSE: Creating StorageAccountCredential inline
VERBOSE: Found storage account with name : contoso76
VERBOSE: Storage credential verification succeeded. 
VERBOSE: Encryption in progress... 
VERBOSE: ClientRequestId: d4f8a5de-bf81-4773-b6e6-edb034284cf4_PS


JobId        : 2dec64d3-b30d-4d35-adb3-12689b235b79
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, 
               Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The job created for your create operation has completed successfully. 
VERBOSE: ClientRequestId: abd4082a-2eda-42ad-8cb3-5864dd2f7d1f_PS
BandwidthRate                   : 256
EncryptionKey                   : SK23I39L7GvoLce7u63TMT/A/V/TW8JXe+PoXKEKzwsr3t/h7tdqV1EpfaK0DGO/qo5b2PLCagFHAxnZEiejg
                                  jtF9TcyK+aLyzEnkqtM+eNRJmgANzJ9C/5L6Ubp+eSWiy+U/pyZygxPrb37e0yFg+qbHV9R9Qi+afBpHD9Gsi
                                  rhURuOc/idWG29eaEifuRzn/zEjvwJ2pEyYLcsuL+ftfRYZom69XO+cRDv5yT3xdNI/dAod/5YUaf1IhJl8wR
                                  cWjqyr00NxlCI03hTgH2sFyTFZWc07S2KI5K5n3rmCL6vGT76SRgNFeUxGz3v06/VoBhdmv9vDfrEz5UkW04d
                                  Qw==
InstanceId                      : a72bf4bb-0f0a-4ec2-a8b1-c4548825f522
IsDefault                       : False
IsEncryptionEnabled             : True
Name                            : VolumneContainer_06
OperationInProgress             : None
Owned                           : True
PrimaryStorageAccountCredential : Microsoft.WindowsAzure.Management.StorSimple.Models.StorageAccountCredentialResponse
SecretsEncryptionThumbprint     : 
VolumeCount                     : 0
```

<span data-ttu-id="1e7d1-112">Det här kommandot skapar ett inline-autentiseringsuppgifter för lagrings konto och skickar sedan vidare till cmdleten **New-AzureStorSimpleDeviceVolumeContainer** med hjälp av operatören.</span><span class="sxs-lookup"><span data-stu-id="1e7d1-112">This command creates a storage account credential inline, and then passes it to the **New-AzureStorSimpleDeviceVolumeContainer** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1e7d1-113">Den behållaren använder provdocka-autentiseringsuppgiften för att skapa en volym behållare.</span><span class="sxs-lookup"><span data-stu-id="1e7d1-113">That container uses the dummy credential to create a volume container.</span></span>

## <span data-ttu-id="1e7d1-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1e7d1-114">PARAMETERS</span></span>

### <span data-ttu-id="1e7d1-115">-Slut punkt</span><span class="sxs-lookup"><span data-stu-id="1e7d1-115">-Endpoint</span></span>
<span data-ttu-id="1e7d1-116">Anger lagrings kontots plats för Azure-lagring.</span><span class="sxs-lookup"><span data-stu-id="1e7d1-116">Specifies the Azure storage endpoint for the storage account.</span></span>

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

### <span data-ttu-id="1e7d1-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="1e7d1-117">-Profile</span></span>
<span data-ttu-id="1e7d1-118">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="1e7d1-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1e7d1-119">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="1e7d1-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1e7d1-120">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="1e7d1-120">-StorageAccountKey</span></span>
<span data-ttu-id="1e7d1-121">Anger lagrings kontots konto nycklar som oformaterad text.</span><span class="sxs-lookup"><span data-stu-id="1e7d1-121">Specifies the account key of the storage account in plain text.</span></span>
<span data-ttu-id="1e7d1-122">Knappen överförs i krypterat format.</span><span class="sxs-lookup"><span data-stu-id="1e7d1-122">The key is transferred in encrypted format.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Key

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e7d1-123">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1e7d1-123">-StorageAccountName</span></span>
<span data-ttu-id="1e7d1-124">Anger namnet på ett befintligt lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="1e7d1-124">Specifies the name of an existing storage account.</span></span>

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

### <span data-ttu-id="1e7d1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e7d1-125">CommonParameters</span></span>
<span data-ttu-id="1e7d1-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e7d1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e7d1-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e7d1-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e7d1-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1e7d1-128">INPUTS</span></span>

### <span data-ttu-id="1e7d1-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="1e7d1-129">None</span></span>

## <span data-ttu-id="1e7d1-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1e7d1-130">OUTPUTS</span></span>

### <span data-ttu-id="1e7d1-131">StorageAccountCredentialResponse</span><span class="sxs-lookup"><span data-stu-id="1e7d1-131">StorageAccountCredentialResponse</span></span>
<span data-ttu-id="1e7d1-132">Denna cmdlet returnerar ett **CloudType** -objekt som innehåller följande fält:</span><span class="sxs-lookup"><span data-stu-id="1e7d1-132">This cmdlet returns a **CloudType** object, which contains the following fields:</span></span> 

- <span data-ttu-id="1e7d1-133">**Värdnamn**.</span><span class="sxs-lookup"><span data-stu-id="1e7d1-133">**Hostname**.</span></span>
<span data-ttu-id="1e7d1-134">**Sträng**.</span><span class="sxs-lookup"><span data-stu-id="1e7d1-134">**String**.</span></span> 
- <span data-ttu-id="1e7d1-135">**InstanceID**.</span><span class="sxs-lookup"><span data-stu-id="1e7d1-135">**InstanceId**.</span></span>
<span data-ttu-id="1e7d1-136">**Sträng**.</span><span class="sxs-lookup"><span data-stu-id="1e7d1-136">**String**.</span></span> 
- <span data-ttu-id="1e7d1-137">**IsDefault**.</span><span class="sxs-lookup"><span data-stu-id="1e7d1-137">**IsDefault**.</span></span>
<span data-ttu-id="1e7d1-138">**Boolean**.</span><span class="sxs-lookup"><span data-stu-id="1e7d1-138">**Boolean**.</span></span> 
- <span data-ttu-id="1e7d1-139">**Plats**.</span><span class="sxs-lookup"><span data-stu-id="1e7d1-139">**Location**.</span></span>
<span data-ttu-id="1e7d1-140">**Sträng**.</span><span class="sxs-lookup"><span data-stu-id="1e7d1-140">**String**.</span></span> 
- <span data-ttu-id="1e7d1-141">**Logga in**.</span><span class="sxs-lookup"><span data-stu-id="1e7d1-141">**Login**.</span></span>
<span data-ttu-id="1e7d1-142">**Sträng**.</span><span class="sxs-lookup"><span data-stu-id="1e7d1-142">**String**.</span></span> 
- <span data-ttu-id="1e7d1-143">**Namn**.</span><span class="sxs-lookup"><span data-stu-id="1e7d1-143">**Name**.</span></span>
<span data-ttu-id="1e7d1-144">**Sträng**.</span><span class="sxs-lookup"><span data-stu-id="1e7d1-144">**String**.</span></span> 
- <span data-ttu-id="1e7d1-145">**OperationInProgress**.</span><span class="sxs-lookup"><span data-stu-id="1e7d1-145">**OperationInProgress**.</span></span>
<span data-ttu-id="1e7d1-146">**OperationInProgress**.</span><span class="sxs-lookup"><span data-stu-id="1e7d1-146">**OperationInProgress**.</span></span> 
- <span data-ttu-id="1e7d1-147">**Lösen ord**.</span><span class="sxs-lookup"><span data-stu-id="1e7d1-147">**Password**.</span></span>
<span data-ttu-id="1e7d1-148">**Sträng**.</span><span class="sxs-lookup"><span data-stu-id="1e7d1-148">**String**.</span></span> 
- <span data-ttu-id="1e7d1-149">**PasswordEncryptionCertThumbprint**.</span><span class="sxs-lookup"><span data-stu-id="1e7d1-149">**PasswordEncryptionCertThumbprint**.</span></span>
<span data-ttu-id="1e7d1-150">**Sträng**.</span><span class="sxs-lookup"><span data-stu-id="1e7d1-150">**String**.</span></span> 
- <span data-ttu-id="1e7d1-151">**UseSSL**.</span><span class="sxs-lookup"><span data-stu-id="1e7d1-151">**UseSSL**.</span></span>
<span data-ttu-id="1e7d1-152">**Boolean**.</span><span class="sxs-lookup"><span data-stu-id="1e7d1-152">**Boolean**.</span></span> 
- <span data-ttu-id="1e7d1-153">**VolumeCount**.</span><span class="sxs-lookup"><span data-stu-id="1e7d1-153">**VolumeCount**.</span></span>
<span data-ttu-id="1e7d1-154">**Heltal**.</span><span class="sxs-lookup"><span data-stu-id="1e7d1-154">**Integer**.</span></span>

## <span data-ttu-id="1e7d1-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1e7d1-155">NOTES</span></span>

## <span data-ttu-id="1e7d1-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1e7d1-156">RELATED LINKS</span></span>

[<span data-ttu-id="1e7d1-157">New-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="1e7d1-157">New-AzureStorSimpleStorageAccountCredential</span></span>](./New-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="1e7d1-158">New-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="1e7d1-158">New-AzureStorSimpleDeviceVolumeContainer</span></span>](./New-AzureStorSimpleDeviceVolumeContainer.md)


