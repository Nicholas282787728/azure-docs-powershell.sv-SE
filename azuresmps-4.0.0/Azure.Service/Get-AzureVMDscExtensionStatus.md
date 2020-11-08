---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 19A87B24-C5A6-4505-BB54-973B24BCC68E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 821927fc465ed5af048a2f27ed84da8c12b9caa5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099766"
---
# <span data-ttu-id="66634-101">Get-AzureVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="66634-101">Get-AzureVMDscExtensionStatus</span></span>

## <span data-ttu-id="66634-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="66634-102">SYNOPSIS</span></span>
<span data-ttu-id="66634-103">Hämtar DSC-filtillägg för alla virtuella datorer som distribuerats i en moln tjänst eller för en viss virtuell dator i tjänsten.</span><span class="sxs-lookup"><span data-stu-id="66634-103">Gets the DSC extension status for all the virtual machines deployed in a cloud service or for a particular virtual machine in the service.</span></span>

## <span data-ttu-id="66634-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="66634-104">SYNTAX</span></span>

### <span data-ttu-id="66634-105">GetStatusByServiceAndVMName (standard)</span><span class="sxs-lookup"><span data-stu-id="66634-105">GetStatusByServiceAndVMName (Default)</span></span>
```
Get-AzureVMDscExtensionStatus [-ServiceName] <String> [[-Name] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="66634-106">GetStatusByVM</span><span class="sxs-lookup"><span data-stu-id="66634-106">GetStatusByVM</span></span>
```
Get-AzureVMDscExtensionStatus -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="66634-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="66634-107">DESCRIPTION</span></span>
<span data-ttu-id="66634-108">Cmdleten **Get-AzureVMDscExtensionStatus** får statusen för önskad tillstånds konfiguration (DSC) för alla virtuella datorer som distribueras i en moln tjänst eller för en viss virtuell dator i tjänsten.</span><span class="sxs-lookup"><span data-stu-id="66634-108">The **Get-AzureVMDscExtensionStatus** cmdlet gets the Desired State Configuration (DSC) extension status for all the virtual machines deployed in a cloud service or for a particular virtual machine in the service.</span></span>

## <span data-ttu-id="66634-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="66634-109">EXAMPLES</span></span>

### <span data-ttu-id="66634-110">9.1</span><span class="sxs-lookup"><span data-stu-id="66634-110">1:</span></span>
```

```

## <span data-ttu-id="66634-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="66634-111">PARAMETERS</span></span>

### <span data-ttu-id="66634-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="66634-112">-InformationAction</span></span>
<span data-ttu-id="66634-113">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="66634-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="66634-114">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="66634-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="66634-115">Vidare</span><span class="sxs-lookup"><span data-stu-id="66634-115">Continue</span></span>
- <span data-ttu-id="66634-116">Över</span><span class="sxs-lookup"><span data-stu-id="66634-116">Ignore</span></span>
- <span data-ttu-id="66634-117">Inquire</span><span class="sxs-lookup"><span data-stu-id="66634-117">Inquire</span></span>
- <span data-ttu-id="66634-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="66634-118">SilentlyContinue</span></span>
- <span data-ttu-id="66634-119">Stanna</span><span class="sxs-lookup"><span data-stu-id="66634-119">Stop</span></span>
- <span data-ttu-id="66634-120">Avbryt</span><span class="sxs-lookup"><span data-stu-id="66634-120">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66634-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="66634-121">-InformationVariable</span></span>
<span data-ttu-id="66634-122">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="66634-122">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66634-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="66634-123">-Name</span></span>
<span data-ttu-id="66634-124">Anger namnet på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="66634-124">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: GetStatusByServiceAndVMName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66634-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="66634-125">-Profile</span></span>
<span data-ttu-id="66634-126">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="66634-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="66634-127">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="66634-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="66634-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="66634-128">-ServiceName</span></span>
<span data-ttu-id="66634-129">Anger namnet på tjänsten.</span><span class="sxs-lookup"><span data-stu-id="66634-129">Specifies the name of the service.</span></span>

```yaml
Type: String
Parameter Sets: GetStatusByServiceAndVMName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66634-130">-VM</span><span class="sxs-lookup"><span data-stu-id="66634-130">-VM</span></span>
<span data-ttu-id="66634-131">Anger permanent virtuell dator-objekt.</span><span class="sxs-lookup"><span data-stu-id="66634-131">Specifies the persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: GetStatusByVM
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66634-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66634-132">CommonParameters</span></span>
<span data-ttu-id="66634-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66634-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66634-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66634-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66634-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="66634-135">INPUTS</span></span>

## <span data-ttu-id="66634-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="66634-136">OUTPUTS</span></span>

### <span data-ttu-id="66634-137">Microsoft. WindowsAzure. kommandon. ServiceManagement. IaaS. Extensions. VirtualMachineDscExtensionStatusContext</span><span class="sxs-lookup"><span data-stu-id="66634-137">Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.VirtualMachineDscExtensionStatusContext</span></span>

## <span data-ttu-id="66634-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="66634-138">NOTES</span></span>

## <span data-ttu-id="66634-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="66634-139">RELATED LINKS</span></span>

[<span data-ttu-id="66634-140">Get-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="66634-140">Get-AzureVMDscExtension</span></span>](./Get-AzureVMDscExtension.md)

[<span data-ttu-id="66634-141">Remove-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="66634-141">Remove-AzureVMDscExtension</span></span>](./Remove-AzureVMDscExtension.md)

[<span data-ttu-id="66634-142">Set-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="66634-142">Set-AzureVMDscExtension</span></span>](./Set-AzureVMDscExtension.md)


