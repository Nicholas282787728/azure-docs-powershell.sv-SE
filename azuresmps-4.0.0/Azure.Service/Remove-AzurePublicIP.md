---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9EA98944-1923-4573-991E-3B9CA21004BB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2f16b51dc8abf5c6243b4b489789d65029acc3c4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099378"
---
# <span data-ttu-id="49ce5-101">Remove-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="49ce5-101">Remove-AzurePublicIP</span></span>

## <span data-ttu-id="49ce5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="49ce5-102">SYNOPSIS</span></span>
<span data-ttu-id="49ce5-103">Tar bort offentlig IP-konfiguration från en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="49ce5-103">Removes Public IP configuration from an Azure virtual machine.</span></span>

## <span data-ttu-id="49ce5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="49ce5-104">SYNTAX</span></span>

```
Remove-AzurePublicIP [[-PublicIPName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="49ce5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="49ce5-105">DESCRIPTION</span></span>
<span data-ttu-id="49ce5-106">Cmdleten **Remove-AzurePublicIP** tar bort offentlig IP-konfiguration från en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="49ce5-106">The **Remove-AzurePublicIP** cmdlet removes Public IP configuration from an Azure virtual machine.</span></span>

## <span data-ttu-id="49ce5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="49ce5-107">EXAMPLES</span></span>

### <span data-ttu-id="49ce5-108">Exempel 1: ta bort offentlig IP-konfiguration</span><span class="sxs-lookup"><span data-stu-id="49ce5-108">Example 1: Remove Public IP configuration</span></span>
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Remove-AzurePublicIP | Update-AzureVM
```

<span data-ttu-id="49ce5-109">Det här kommandot får den virtuella datorn som heter FTPInstance i tjänsten FTPInAzure med hjälp av cmdleten **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="49ce5-109">This command gets the virtual machine named FTPInstance in the service named FTPInAzure by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="49ce5-110">Kommandot skickar den virtuella datorn till den aktuella cmdleten med operatören.</span><span class="sxs-lookup"><span data-stu-id="49ce5-110">The command passes that virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="49ce5-111">Den aktuella cmdleten tar bort offentlig IP-konfiguration från den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="49ce5-111">The current cmdlet removes Public IP configuration from the virtual machine.</span></span>
<span data-ttu-id="49ce5-112">Kommandot skickar den virtuella datorn till cmdleten **Update-AzureVM** som implementerar dina ändringar.</span><span class="sxs-lookup"><span data-stu-id="49ce5-112">The command passes the virtual machine to the **Update-AzureVM** cmdlet, which implements your changes.</span></span>

## <span data-ttu-id="49ce5-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="49ce5-113">PARAMETERS</span></span>

### <span data-ttu-id="49ce5-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="49ce5-114">-InformationAction</span></span>
<span data-ttu-id="49ce5-115">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="49ce5-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="49ce5-116">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="49ce5-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="49ce5-117">Vidare</span><span class="sxs-lookup"><span data-stu-id="49ce5-117">Continue</span></span>
- <span data-ttu-id="49ce5-118">Över</span><span class="sxs-lookup"><span data-stu-id="49ce5-118">Ignore</span></span>
- <span data-ttu-id="49ce5-119">Inquire</span><span class="sxs-lookup"><span data-stu-id="49ce5-119">Inquire</span></span>
- <span data-ttu-id="49ce5-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="49ce5-120">SilentlyContinue</span></span>
- <span data-ttu-id="49ce5-121">Stanna</span><span class="sxs-lookup"><span data-stu-id="49ce5-121">Stop</span></span>
- <span data-ttu-id="49ce5-122">Avbryt</span><span class="sxs-lookup"><span data-stu-id="49ce5-122">Suspend</span></span>

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

### <span data-ttu-id="49ce5-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="49ce5-123">-InformationVariable</span></span>
<span data-ttu-id="49ce5-124">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="49ce5-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="49ce5-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="49ce5-125">-Profile</span></span>
<span data-ttu-id="49ce5-126">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="49ce5-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="49ce5-127">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="49ce5-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="49ce5-128">-PublicIPName</span><span class="sxs-lookup"><span data-stu-id="49ce5-128">-PublicIPName</span></span>
<span data-ttu-id="49ce5-129">Anger det offentliga IP-namnet.</span><span class="sxs-lookup"><span data-stu-id="49ce5-129">Specifies the Public IP name.</span></span>

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

### <span data-ttu-id="49ce5-130">-VM</span><span class="sxs-lookup"><span data-stu-id="49ce5-130">-VM</span></span>
<span data-ttu-id="49ce5-131">Anger den virtuella dator som den här cmdleten tar bort offentlig IP-konfiguration från.</span><span class="sxs-lookup"><span data-stu-id="49ce5-131">Specifies the virtual machine from which this cmdlet removes Public IP configuration.</span></span>

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

### <span data-ttu-id="49ce5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49ce5-132">CommonParameters</span></span>
<span data-ttu-id="49ce5-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49ce5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49ce5-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49ce5-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49ce5-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="49ce5-135">INPUTS</span></span>

## <span data-ttu-id="49ce5-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="49ce5-136">OUTPUTS</span></span>

### <span data-ttu-id="49ce5-137">Microsoft. WindowsAzure. kommandon. ServiceManagement. Model. IPersistentVM</span><span class="sxs-lookup"><span data-stu-id="49ce5-137">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.IPersistentVM</span></span>

## <span data-ttu-id="49ce5-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="49ce5-138">NOTES</span></span>

## <span data-ttu-id="49ce5-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="49ce5-139">RELATED LINKS</span></span>

[<span data-ttu-id="49ce5-140">Get-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="49ce5-140">Get-AzurePublicIP</span></span>](./Get-AzurePublicIP.md)

[<span data-ttu-id="49ce5-141">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="49ce5-141">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="49ce5-142">Set-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="49ce5-142">Set-AzurePublicIP</span></span>](./Set-AzurePublicIP.md)

[<span data-ttu-id="49ce5-143">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="49ce5-143">Update-AzureVM</span></span>](./Update-AzureVM.md)


