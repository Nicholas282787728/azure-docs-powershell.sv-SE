---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9D6D1890-9442-45F1-A3AA-BB1DB5CB33D6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 462d40e463edf6894810ac6e00e39b9c7a9eabe1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099768"
---
# <span data-ttu-id="58a3b-101">Get-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="58a3b-101">Get-AzureVMDscExtension</span></span>

## <span data-ttu-id="58a3b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="58a3b-102">SYNOPSIS</span></span>
<span data-ttu-id="58a3b-103">Hämtar inställningarna för DSC-tillägget på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="58a3b-103">Gets the settings of the DSC extension on a virtual machine.</span></span>

## <span data-ttu-id="58a3b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="58a3b-104">SYNTAX</span></span>

```
Get-AzureVMDscExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="58a3b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="58a3b-105">DESCRIPTION</span></span>
<span data-ttu-id="58a3b-106">Cmdleten **Get-AzureVMDscExtension** hämtar inställningarna för DSC-tillägget på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="58a3b-106">The **Get-AzureVMDscExtension** cmdlet gets the settings of the DSC extension on a virtual machine.</span></span>

## <span data-ttu-id="58a3b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="58a3b-107">EXAMPLES</span></span>

### <span data-ttu-id="58a3b-108">Exempel 1: Hämta DSC-tillägget på en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="58a3b-108">Example 1: Get the setting of the DSC Extension on a virtual machine</span></span>
```
PS C:\> Get-AzureVMDscExtension -VM $VMModulesUrl
https://myaccount.blob.core.contoso.net/windows-powershell-dsc/MyConfiguration.ps1.zipConfigurationFunction : MyConfiguration.ps1\MyConfigurationProperties            : {ServerName}ExtensionName         : DSCPublisher             : Microsoft.PowershellVersion               : 1.*PrivateConfiguration  :PublicConfiguration   : {"ModulesUrl": "https://myaccount.blob.core.contoso.net/windows-powershell-dsc/MyConfiguration.ps1.zip","ConfigurationFunction": "MyConfiguration.ps1\\MyConfiguration","Properties": {"ServerName": "C:\\MyDirectory"}}ReferenceName         : DSCState                 : EnableRoleName              : my-vm
```

<span data-ttu-id="58a3b-109">Det här kommandot får DSC-tilläggets inställningar på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="58a3b-109">This command gets the settings of the DSC Extension on a virtual machine.</span></span>

## <span data-ttu-id="58a3b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="58a3b-110">PARAMETERS</span></span>

### <span data-ttu-id="58a3b-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="58a3b-111">-InformationAction</span></span>
<span data-ttu-id="58a3b-112">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="58a3b-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="58a3b-113">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="58a3b-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="58a3b-114">Vidare</span><span class="sxs-lookup"><span data-stu-id="58a3b-114">Continue</span></span>
- <span data-ttu-id="58a3b-115">Över</span><span class="sxs-lookup"><span data-stu-id="58a3b-115">Ignore</span></span>
- <span data-ttu-id="58a3b-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="58a3b-116">Inquire</span></span>
- <span data-ttu-id="58a3b-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="58a3b-117">SilentlyContinue</span></span>
- <span data-ttu-id="58a3b-118">Stanna</span><span class="sxs-lookup"><span data-stu-id="58a3b-118">Stop</span></span>
- <span data-ttu-id="58a3b-119">Avbryt</span><span class="sxs-lookup"><span data-stu-id="58a3b-119">Suspend</span></span>

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

### <span data-ttu-id="58a3b-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="58a3b-120">-InformationVariable</span></span>
<span data-ttu-id="58a3b-121">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="58a3b-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="58a3b-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="58a3b-122">-Profile</span></span>
<span data-ttu-id="58a3b-123">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="58a3b-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="58a3b-124">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="58a3b-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="58a3b-125">-VM</span><span class="sxs-lookup"><span data-stu-id="58a3b-125">-VM</span></span>
<span data-ttu-id="58a3b-126">Anger permanent virtuell dator-objekt.</span><span class="sxs-lookup"><span data-stu-id="58a3b-126">Specifies the persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58a3b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58a3b-127">CommonParameters</span></span>
<span data-ttu-id="58a3b-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58a3b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58a3b-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58a3b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58a3b-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="58a3b-130">INPUTS</span></span>

## <span data-ttu-id="58a3b-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="58a3b-131">OUTPUTS</span></span>

### <span data-ttu-id="58a3b-132">Microsoft. WindowsAzure. kommandon. ServiceManagement. IaaS. Extensions. VirtualMachineDscExtensionContext</span><span class="sxs-lookup"><span data-stu-id="58a3b-132">Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.VirtualMachineDscExtensionContext</span></span>

## <span data-ttu-id="58a3b-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="58a3b-133">NOTES</span></span>

## <span data-ttu-id="58a3b-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="58a3b-134">RELATED LINKS</span></span>

[<span data-ttu-id="58a3b-135">Remove-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="58a3b-135">Remove-AzureVMDscExtension</span></span>](./Remove-AzureVMDscExtension.md)

[<span data-ttu-id="58a3b-136">Set-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="58a3b-136">Set-AzureVMDscExtension</span></span>](./Set-AzureVMDscExtension.md)

[<span data-ttu-id="58a3b-137">Get-AzureVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="58a3b-137">Get-AzureVMDscExtensionStatus</span></span>](./Get-AzureVMDscExtensionStatus.md)


