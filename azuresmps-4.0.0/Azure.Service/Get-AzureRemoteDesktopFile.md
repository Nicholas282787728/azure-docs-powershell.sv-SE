---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8A6B2633-EECC-416A-85F6-69C8341AA970
online version: ''
schema: 2.0.0
ms.openlocfilehash: 82ef50dcdf5f17e044a9dc2091cbfda5cb5d1b2a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093346"
---
# <span data-ttu-id="568cb-101">Get-AzureRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="568cb-101">Get-AzureRemoteDesktopFile</span></span>

## <span data-ttu-id="568cb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="568cb-102">SYNOPSIS</span></span>
<span data-ttu-id="568cb-103">Hämtar en RDP-fil för en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="568cb-103">Gets an RDP file for an Azure virtual machine.</span></span>

## <span data-ttu-id="568cb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="568cb-104">SYNTAX</span></span>

### <span data-ttu-id="568cb-105">Ladda ned (standard)</span><span class="sxs-lookup"><span data-stu-id="568cb-105">Download (Default)</span></span>
```
Get-AzureRemoteDesktopFile [-Name] <String> [-LocalPath] <String> [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="568cb-106">Start</span><span class="sxs-lookup"><span data-stu-id="568cb-106">Launch</span></span>
```
Get-AzureRemoteDesktopFile [-Name] <String> [[-LocalPath] <String>] [-Launch] [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="568cb-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="568cb-107">DESCRIPTION</span></span>
<span data-ttu-id="568cb-108">Cmdleten **Get-AzureRemoteDesktopFile** -Ladda ner och sparar en RDP-fil (Remote Desktop Connection) för en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="568cb-108">The **Get-AzureRemoteDesktopFile** cmdlet downloads and saves a remote desktop connection (RDP) file for an Azure virtual machine.</span></span>
<span data-ttu-id="568cb-109">Cmdleten kan starta en fjärr skrivbords anslutning till den angivna virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="568cb-109">The cmdlet can launch a remote desktop connection to the specified virtual machine.</span></span>

## <span data-ttu-id="568cb-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="568cb-110">EXAMPLES</span></span>

### <span data-ttu-id="568cb-111">Exempel 1: Hämta en RDP-fil</span><span class="sxs-lookup"><span data-stu-id="568cb-111">Example 1: Get an RDP file</span></span>
```
PS C:\> Get-AzureRemoteDesktopFile -ServiceName "ContosoService" -Name "VirtualMachine07" -LocalPath "C:\temp\VirtualMachine07.rdp"
```

<span data-ttu-id="568cb-112">Det här kommandot får en RDP-fil för den virtuella datorn VirtualMachine07 med namnet VirtualMachine07 som körs på tjänsten som heter ContosoService.</span><span class="sxs-lookup"><span data-stu-id="568cb-112">This command gets an RDP file for the VirtualMachine07 virtual machine named VirtualMachine07 that runs on the service named ContosoService.</span></span>
<span data-ttu-id="568cb-113">Kommandot sparar filen som C:\temp\VirtualMachine07.rdp.</span><span class="sxs-lookup"><span data-stu-id="568cb-113">The command stores that file as C:\temp\VirtualMachine07.rdp.</span></span>

### <span data-ttu-id="568cb-114">Exempel 2: starta en fjärrsession</span><span class="sxs-lookup"><span data-stu-id="568cb-114">Example 2: Start a remote session</span></span>
```
PS C:\> Get-AzureRemoteDesktopFile -ServiceName "ContosoService" -Name "VirtualMachine07" -Launch
```

<span data-ttu-id="568cb-115">Det här kommandot får en RDP-fil för den virtuella datorn VirtualMachine07 med namnet VirtualMachine07 som körs på tjänsten som heter ContosoService.</span><span class="sxs-lookup"><span data-stu-id="568cb-115">This command gets an RDP file for the VirtualMachine07 virtual machine named VirtualMachine07 that runs on the service named ContosoService.</span></span>
<span data-ttu-id="568cb-116">Kommandot startar en fjärrskrivbordssession.</span><span class="sxs-lookup"><span data-stu-id="568cb-116">The command launches a remote desktop session.</span></span>
<span data-ttu-id="568cb-117">Kommandot tar bort RDP-filen när anslutningen är stängd.</span><span class="sxs-lookup"><span data-stu-id="568cb-117">The command deletes the RDP file when the connection is closed.</span></span>

## <span data-ttu-id="568cb-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="568cb-118">PARAMETERS</span></span>

### <span data-ttu-id="568cb-119">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="568cb-119">-InformationAction</span></span>
<span data-ttu-id="568cb-120">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="568cb-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="568cb-121">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="568cb-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="568cb-122">Vidare</span><span class="sxs-lookup"><span data-stu-id="568cb-122">Continue</span></span>
- <span data-ttu-id="568cb-123">Över</span><span class="sxs-lookup"><span data-stu-id="568cb-123">Ignore</span></span>
- <span data-ttu-id="568cb-124">Inquire</span><span class="sxs-lookup"><span data-stu-id="568cb-124">Inquire</span></span>
- <span data-ttu-id="568cb-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="568cb-125">SilentlyContinue</span></span>
- <span data-ttu-id="568cb-126">Stanna</span><span class="sxs-lookup"><span data-stu-id="568cb-126">Stop</span></span>
- <span data-ttu-id="568cb-127">Avbryt</span><span class="sxs-lookup"><span data-stu-id="568cb-127">Suspend</span></span>

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

### <span data-ttu-id="568cb-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="568cb-128">-InformationVariable</span></span>
<span data-ttu-id="568cb-129">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="568cb-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="568cb-130">-Lansera</span><span class="sxs-lookup"><span data-stu-id="568cb-130">-Launch</span></span>
<span data-ttu-id="568cb-131">Anger att den här cmdleten startar en fjärr skrivbords-session till den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="568cb-131">Indicates that this cmdlet starts a remote desktop session to the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Launch
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="568cb-132">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="568cb-132">-LocalPath</span></span>
<span data-ttu-id="568cb-133">Anger den fullständiga sökvägen till den nedladdade RDP-filen på den lokala datorn.</span><span class="sxs-lookup"><span data-stu-id="568cb-133">Specifies the full path of the downloaded RDP file on the local computer.</span></span>

```yaml
Type: String
Parameter Sets: Download
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Launch
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="568cb-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="568cb-134">-Name</span></span>
<span data-ttu-id="568cb-135">Anger den virtuella dator för vilken denna cmdlet laddar ned en RDP-fil.</span><span class="sxs-lookup"><span data-stu-id="568cb-135">Specifies the virtual machine for which this cmdlet downloads an RDP file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: InstanceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="568cb-136">-Profil</span><span class="sxs-lookup"><span data-stu-id="568cb-136">-Profile</span></span>
<span data-ttu-id="568cb-137">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="568cb-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="568cb-138">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="568cb-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="568cb-139">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="568cb-139">-ServiceName</span></span>
<span data-ttu-id="568cb-140">Anger namnet på den Azure-tjänst som den virtuella datorn tillhör.</span><span class="sxs-lookup"><span data-stu-id="568cb-140">Specifies the name of the Azure service to which the virtual machine belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="568cb-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="568cb-141">CommonParameters</span></span>
<span data-ttu-id="568cb-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="568cb-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="568cb-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="568cb-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="568cb-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="568cb-144">INPUTS</span></span>

## <span data-ttu-id="568cb-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="568cb-145">OUTPUTS</span></span>

## <span data-ttu-id="568cb-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="568cb-146">NOTES</span></span>

## <span data-ttu-id="568cb-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="568cb-147">RELATED LINKS</span></span>

