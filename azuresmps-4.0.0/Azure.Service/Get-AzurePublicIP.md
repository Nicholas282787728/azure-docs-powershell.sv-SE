---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5BEE9430-D6BF-49F1-A23D-32784C6C818E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 98b9abe6bcb9998067fe978a5f99f5d8b64cd26d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099561"
---
# <span data-ttu-id="3b86c-101">Get-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="3b86c-101">Get-AzurePublicIP</span></span>

## <span data-ttu-id="3b86c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3b86c-102">SYNOPSIS</span></span>
<span data-ttu-id="3b86c-103">Hämtar den offentliga IP-informationen för en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="3b86c-103">Gets the Public IP information for an Azure virtual machine.</span></span>

## <span data-ttu-id="3b86c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3b86c-104">SYNTAX</span></span>

```
Get-AzurePublicIP [[-PublicIPName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3b86c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3b86c-105">DESCRIPTION</span></span>
<span data-ttu-id="3b86c-106">Cmdleten **Get-AzurePublicIP** hämtar den offentliga IP-informationen för en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="3b86c-106">The **Get-AzurePublicIP** cmdlet gets the Public IP information for an Azure virtual machine.</span></span>
<span data-ttu-id="3b86c-107">Använd cmdleten **Get-AzureVM** för att få IP-adressen till den offentliga IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="3b86c-107">To obtain the IP address of the Public IP, use the **Get-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="3b86c-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3b86c-108">EXAMPLES</span></span>

### <span data-ttu-id="3b86c-109">Exempel 1: Hämta offentlig IP-konfiguration</span><span class="sxs-lookup"><span data-stu-id="3b86c-109">Example 1: Get Public IP configuration</span></span>
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Get-AzurePublicIP
```

<span data-ttu-id="3b86c-110">Det här kommandot får den virtuella datorn som heter FTPInstance i tjänsten FTPInAzure med hjälp av cmdleten **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="3b86c-110">This command gets the virtual machine named FTPInstance in the service named FTPInAzure by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="3b86c-111">Kommandot skickar den virtuella datorn till den aktuella cmdleten med operatören.</span><span class="sxs-lookup"><span data-stu-id="3b86c-111">The command passes that virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3b86c-112">Den aktuella cmdleten hämtar offentlig IP-konfiguration från den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="3b86c-112">The current cmdlet gets Public IP configuration from the virtual machine.</span></span>

## <span data-ttu-id="3b86c-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3b86c-113">PARAMETERS</span></span>

### <span data-ttu-id="3b86c-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3b86c-114">-InformationAction</span></span>
<span data-ttu-id="3b86c-115">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="3b86c-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3b86c-116">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="3b86c-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3b86c-117">Vidare</span><span class="sxs-lookup"><span data-stu-id="3b86c-117">Continue</span></span>
- <span data-ttu-id="3b86c-118">Över</span><span class="sxs-lookup"><span data-stu-id="3b86c-118">Ignore</span></span>
- <span data-ttu-id="3b86c-119">Inquire</span><span class="sxs-lookup"><span data-stu-id="3b86c-119">Inquire</span></span>
- <span data-ttu-id="3b86c-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3b86c-120">SilentlyContinue</span></span>
- <span data-ttu-id="3b86c-121">Stanna</span><span class="sxs-lookup"><span data-stu-id="3b86c-121">Stop</span></span>
- <span data-ttu-id="3b86c-122">Avbryt</span><span class="sxs-lookup"><span data-stu-id="3b86c-122">Suspend</span></span>

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

### <span data-ttu-id="3b86c-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3b86c-123">-InformationVariable</span></span>
<span data-ttu-id="3b86c-124">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="3b86c-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="3b86c-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="3b86c-125">-Profile</span></span>
<span data-ttu-id="3b86c-126">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="3b86c-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3b86c-127">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="3b86c-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3b86c-128">-PublicIPName</span><span class="sxs-lookup"><span data-stu-id="3b86c-128">-PublicIPName</span></span>
<span data-ttu-id="3b86c-129">Anger det offentliga IP-namnet.</span><span class="sxs-lookup"><span data-stu-id="3b86c-129">Specifies the Public IP name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b86c-130">-VM</span><span class="sxs-lookup"><span data-stu-id="3b86c-130">-VM</span></span>
<span data-ttu-id="3b86c-131">Anger den virtuella dator för vilken denna cmdlet hämtar offentlig IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="3b86c-131">Specifies the virtual machine for which this cmdlet gets Public IP configuration.</span></span>

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

### <span data-ttu-id="3b86c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b86c-132">CommonParameters</span></span>
<span data-ttu-id="3b86c-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b86c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b86c-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b86c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b86c-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3b86c-135">INPUTS</span></span>

## <span data-ttu-id="3b86c-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3b86c-136">OUTPUTS</span></span>

### <span data-ttu-id="3b86c-137">Microsoft. WindowsAzure. kommandon. ServiceManagement. AssignPublicIPCollection</span><span class="sxs-lookup"><span data-stu-id="3b86c-137">Microsoft.WindowsAzure.Commands.ServiceManagement.AssignPublicIPCollection</span></span>

## <span data-ttu-id="3b86c-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3b86c-138">NOTES</span></span>

## <span data-ttu-id="3b86c-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3b86c-139">RELATED LINKS</span></span>

[<span data-ttu-id="3b86c-140">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="3b86c-140">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="3b86c-141">Remove-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="3b86c-141">Remove-AzurePublicIP</span></span>](./Remove-AzurePublicIP.md)

[<span data-ttu-id="3b86c-142">Set-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="3b86c-142">Set-AzurePublicIP</span></span>](./Set-AzurePublicIP.md)


