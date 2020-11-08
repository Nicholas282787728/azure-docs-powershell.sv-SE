---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5F827BFB-492E-48A2-9610-0CB5FBDD1F9E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0c66043fa36620c2879e88b7dbf82ba251aa4fbc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099735"
---
# <span data-ttu-id="3f129-101">Get-AzureWinRMUri</span><span class="sxs-lookup"><span data-stu-id="3f129-101">Get-AzureWinRMUri</span></span>

## <span data-ttu-id="3f129-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3f129-102">SYNOPSIS</span></span>
<span data-ttu-id="3f129-103">Hämtar URI-lyssningen till en virtuell dator eller en lista över virtuella datorer i en värd tjänst.</span><span class="sxs-lookup"><span data-stu-id="3f129-103">Gets the URI to WinRM https listener to a virtual machine or a list of virtual machines in a hosted service.</span></span>

## <span data-ttu-id="3f129-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3f129-104">SYNTAX</span></span>

```
Get-AzureWinRMUri [-ServiceName] <String> [[-Name] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3f129-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3f129-105">DESCRIPTION</span></span>
<span data-ttu-id="3f129-106">Cmdleten **Get-AzureWinRMUri** får URI: n för Windows Remote Management (WinRM) https-lyssnaren till en virtuell dator eller en lista över virtuella datorer i en värdbaserad tjänst.</span><span class="sxs-lookup"><span data-stu-id="3f129-106">The **Get-AzureWinRMUri** cmdlet gets the URI of the Windows Remote Management (WinRM) https listener to a virtual machine or a list of virtual machines in a hosted service.</span></span>

## <span data-ttu-id="3f129-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3f129-107">EXAMPLES</span></span>

### <span data-ttu-id="3f129-108">Exempel 1: Hämta URI för WinRM https-lyssnaren till en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="3f129-108">Example 1: Get the URI of the WinRM https listener to a virtual machine</span></span>
```
PS C:\> Get-AzureWinRMUri -ServiceName MyService -Name MyVM
```

<span data-ttu-id="3f129-109">Det här kommandot får UIR för WinRM https-lyssnaren till en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="3f129-109">This command gets the UIR of the WinRM https listener to a virtual machine.</span></span>

### <span data-ttu-id="3f129-110">Exempel 2: Hämta URI för WinRM https-lyssnaren till en virtuell dator för en viss tjänst</span><span class="sxs-lookup"><span data-stu-id="3f129-110">Example 2: Get the URI of the WinRM https listener to a virtual machine of a specific service</span></span>
```
PS C:\> Get-AzureWinRMUri -ServiceName MyService
```

<span data-ttu-id="3f129-111">Det här kommandot får UIR för WinRM https-lyssnaren till en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="3f129-111">This command gets the UIR of the WinRM https listener to a virtual machine.</span></span>

## <span data-ttu-id="3f129-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3f129-112">PARAMETERS</span></span>

### <span data-ttu-id="3f129-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3f129-113">-InformationAction</span></span>
<span data-ttu-id="3f129-114">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="3f129-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3f129-115">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="3f129-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3f129-116">Vidare</span><span class="sxs-lookup"><span data-stu-id="3f129-116">Continue</span></span>
- <span data-ttu-id="3f129-117">Över</span><span class="sxs-lookup"><span data-stu-id="3f129-117">Ignore</span></span>
- <span data-ttu-id="3f129-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="3f129-118">Inquire</span></span>
- <span data-ttu-id="3f129-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3f129-119">SilentlyContinue</span></span>
- <span data-ttu-id="3f129-120">Stanna</span><span class="sxs-lookup"><span data-stu-id="3f129-120">Stop</span></span>
- <span data-ttu-id="3f129-121">Avbryt</span><span class="sxs-lookup"><span data-stu-id="3f129-121">Suspend</span></span>

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

### <span data-ttu-id="3f129-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3f129-122">-InformationVariable</span></span>
<span data-ttu-id="3f129-123">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="3f129-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="3f129-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="3f129-124">-Name</span></span>
<span data-ttu-id="3f129-125">Anger namnet på den virtuella dator som WinRM URI: n genereras till.</span><span class="sxs-lookup"><span data-stu-id="3f129-125">Specifies the name of the virtual machine to which the WinRM URI is generated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f129-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="3f129-126">-Profile</span></span>
<span data-ttu-id="3f129-127">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="3f129-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3f129-128">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="3f129-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3f129-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="3f129-129">-ServiceName</span></span>
<span data-ttu-id="3f129-130">Anger namnet på den Microsoft Azure-tjänst som är värd för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="3f129-130">Specifies the name of the Microsoft Azure service that hosts the virtual machine.</span></span>

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

### <span data-ttu-id="3f129-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f129-131">CommonParameters</span></span>
<span data-ttu-id="3f129-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f129-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f129-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f129-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f129-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3f129-134">INPUTS</span></span>

## <span data-ttu-id="3f129-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3f129-135">OUTPUTS</span></span>

## <span data-ttu-id="3f129-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3f129-136">NOTES</span></span>

## <span data-ttu-id="3f129-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3f129-137">RELATED LINKS</span></span>

[<span data-ttu-id="3f129-138">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="3f129-138">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="3f129-139">New-AzureQuickVM</span><span class="sxs-lookup"><span data-stu-id="3f129-139">New-AzureQuickVM</span></span>](./New-AzureQuickVM.md)


