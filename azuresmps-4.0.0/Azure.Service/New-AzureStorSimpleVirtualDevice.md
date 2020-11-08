---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F16BCE0C-1F2C-4FB7-972D-28BE3CCD96D9
online version: ''
schema: 2.0.0
ms.openlocfilehash: dc41efa1901debf2efabf66f8d27f00da7eafe5f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093237"
---
# <span data-ttu-id="e1da2-101">New-AzureStorSimpleVirtualDevice</span><span class="sxs-lookup"><span data-stu-id="e1da2-101">New-AzureStorSimpleVirtualDevice</span></span>

## <span data-ttu-id="e1da2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e1da2-102">SYNOPSIS</span></span>
<span data-ttu-id="e1da2-103">Skapar en virtuell StorSimple-enhet.</span><span class="sxs-lookup"><span data-stu-id="e1da2-103">Creates a virtual StorSimple device.</span></span>

## <span data-ttu-id="e1da2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e1da2-104">SYNTAX</span></span>

### <span data-ttu-id="e1da2-105">CreateNewStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e1da2-105">CreateNewStorageAccount</span></span>
```
New-AzureStorSimpleVirtualDevice -VirtualDeviceName <String> -VirtualNetworkName <String> -SubNetName <String>
 [-StorageAccountName <String>] [-CreateNewStorageAccount] [-PersistAzureVMOnFailrue]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e1da2-106">UseExistingStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e1da2-106">UseExistingStorageAccount</span></span>
```
New-AzureStorSimpleVirtualDevice -VirtualDeviceName <String> -VirtualNetworkName <String> -SubNetName <String>
 -StorageAccountName <String> [-PersistAzureVMOnFailrue] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e1da2-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e1da2-107">DESCRIPTION</span></span>
<span data-ttu-id="e1da2-108">Cmdleten **New-AzureStorSimpleVirtualDevice** skapar en virtuell StorSimple-enhet.</span><span class="sxs-lookup"><span data-stu-id="e1da2-108">The **New-AzureStorSimpleVirtualDevice** cmdlet creates a virtual StorSimple device.</span></span>
<span data-ttu-id="e1da2-109">Ange ett enhets namn för enheten.</span><span class="sxs-lookup"><span data-stu-id="e1da2-109">Specify a device name for the device.</span></span>
<span data-ttu-id="e1da2-110">Ange information om virtuellt nätverk och undernät för det virtuella nätverket i samma prenumeration.</span><span class="sxs-lookup"><span data-stu-id="e1da2-110">Specify virtual network and subnet details for the virtual network in the same subscription.</span></span>
<span data-ttu-id="e1da2-111">Geo-värdet ska matcha det geo-där StorSimple-resursen skapas.</span><span class="sxs-lookup"><span data-stu-id="e1da2-111">The geo should match the geo in which the StorSimple resource is created.</span></span>
<span data-ttu-id="e1da2-112">Om du vill använda ett befintligt lagrings konto för den här virtuella enheten anger du namnet.</span><span class="sxs-lookup"><span data-stu-id="e1da2-112">To use an existing storage account for this virtual device, specify the name.</span></span>
<span data-ttu-id="e1da2-113">Om du vill skapa ett nytt lagrings konto för den här virtuella enheten anger du både *StorageAccountName* och *CreateNewStorageAccount* .</span><span class="sxs-lookup"><span data-stu-id="e1da2-113">To create a new storage account for this virtual device, specify both the *StorageAccountName* and the *CreateNewStorageAccount* parameters.</span></span>

## <span data-ttu-id="e1da2-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e1da2-114">EXAMPLES</span></span>

### <span data-ttu-id="e1da2-115">Exempel 1: skapa en virtuell enhet med ett nytt konto och ett befintligt nätverk</span><span class="sxs-lookup"><span data-stu-id="e1da2-115">Example 1: Create a virtual device with a new account and an existing network</span></span>
```
PS C:\>New-AzureStorSimpleVirtualDevice -VirtualDeviceName "Contosodevice02" -VirtualNetworkName "Saas2vpn" -SubNetName "TenantSubnet" -StorageAccountName "AzureTenant04" -CreateNewStorageAccount
64e4c564-b0ac-44b0-afb4-adf28ac24ad0
VERBOSE: The create job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId 64e4c564-b0ac-44b0-afb4-adf28ac24ad0 for tracking the job's status
```

<span data-ttu-id="e1da2-116">Det här kommandot skapar en virtuell enhet som använder ett nytt lagrings konto och ett befintligt virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="e1da2-116">This command creates a virtual device that uses a new storage account and an existing virtual network.</span></span>

### <span data-ttu-id="e1da2-117">Exempel 2: skapa en virtuell enhet med ett befintligt konto och virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="e1da2-117">Example 2: Create a virtual device with an existing account and virtual network</span></span>
```
PS C:\>New-AzureStorSimpleVirtualDevice -VirtualDeviceName "ContosoDevice07" -VirtualNetworkName "Saas2vpn" -SubNetName TenantSubnet -StorageAccountName azurecisbvtdnd
2a18a3b7-1ec6-481d-b95d-66ba8f67ceaf
VERBOSE: The create job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId 2a18a3b7-1ec6-481d-b95d-66ba8f67ceaf for tracking the job's status
```

<span data-ttu-id="e1da2-118">Det här kommandot skapar en virtuell enhet som använder ett befintligt lagrings konto och ett befintligt virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="e1da2-118">This command creates a virtual device that uses an existing storage account and an existing virtual network.</span></span>

## <span data-ttu-id="e1da2-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e1da2-119">PARAMETERS</span></span>

### <span data-ttu-id="e1da2-120">-CreateNewStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e1da2-120">-CreateNewStorageAccount</span></span>
<span data-ttu-id="e1da2-121">Anger att denna cmdlet skapar ett nytt lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="e1da2-121">Indicates that this cmdlet creates a new storage account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CreateNewStorageAccount
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1da2-122">-PersistAzureVMOnFailrue</span><span class="sxs-lookup"><span data-stu-id="e1da2-122">-PersistAzureVMOnFailrue</span></span>
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

### <span data-ttu-id="e1da2-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="e1da2-123">-Profile</span></span>
<span data-ttu-id="e1da2-124">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="e1da2-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e1da2-125">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="e1da2-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e1da2-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e1da2-126">-StorageAccountName</span></span>
<span data-ttu-id="e1da2-127">Anger namnet på ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="e1da2-127">Specifies the name of a storage account.</span></span>

```yaml
Type: String
Parameter Sets: CreateNewStorageAccount
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: UseExistingStorageAccount
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1da2-128">-SubNetName</span><span class="sxs-lookup"><span data-stu-id="e1da2-128">-SubNetName</span></span>
<span data-ttu-id="e1da2-129">Anger namnet på ett virtuellt undernät.</span><span class="sxs-lookup"><span data-stu-id="e1da2-129">Specifies the name of a virtual subnet.</span></span>

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

### <span data-ttu-id="e1da2-130">-VirtualDeviceName</span><span class="sxs-lookup"><span data-stu-id="e1da2-130">-VirtualDeviceName</span></span>
<span data-ttu-id="e1da2-131">Anger ett namn för den virtuella enheten.</span><span class="sxs-lookup"><span data-stu-id="e1da2-131">Specifies a name for the virtual device.</span></span>

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

### <span data-ttu-id="e1da2-132">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="e1da2-132">-VirtualNetworkName</span></span>
<span data-ttu-id="e1da2-133">Anger namnet på ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="e1da2-133">Specifies the name of a virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: VNetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1da2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1da2-134">CommonParameters</span></span>
<span data-ttu-id="e1da2-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1da2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1da2-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1da2-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1da2-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e1da2-137">INPUTS</span></span>

## <span data-ttu-id="e1da2-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e1da2-138">OUTPUTS</span></span>

### <span data-ttu-id="e1da2-139">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="e1da2-139">String</span></span>
<span data-ttu-id="e1da2-140">Denna cmdlet returnerar ID för det jobb som skapar den virtuella enheten.</span><span class="sxs-lookup"><span data-stu-id="e1da2-140">This cmdlet returns the ID of the job that creates the virtual device.</span></span>
<span data-ttu-id="e1da2-141">Du kan använda detta ID för att spåra förloppet med Get-AzureStorSimpleJob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1da2-141">You can use this ID to track the progress using the Get-AzureStorSimpleJob cmdlet.</span></span>

## <span data-ttu-id="e1da2-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e1da2-142">NOTES</span></span>

## <span data-ttu-id="e1da2-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e1da2-143">RELATED LINKS</span></span>

[<span data-ttu-id="e1da2-144">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="e1da2-144">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)

[<span data-ttu-id="e1da2-145">Set-AzureStorSimpleVirtualDevice</span><span class="sxs-lookup"><span data-stu-id="e1da2-145">Set-AzureStorSimpleVirtualDevice</span></span>](./Set-AzureStorSimpleVirtualDevice.md)


