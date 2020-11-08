---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1CFB90FD-7BC5-4687-8D08-775097DDA062
online version: ''
schema: 2.0.0
ms.openlocfilehash: 651b38a21dff03ce3c5925040d65bc2967eeaa77
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093371"
---
# <span data-ttu-id="c65a9-101">Get-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="c65a9-101">Get-AzureEndpoint</span></span>

## <span data-ttu-id="c65a9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c65a9-102">SYNOPSIS</span></span>
<span data-ttu-id="c65a9-103">Hämtar information om de slut punkter som har tilldelats en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="c65a9-103">Gets information about the endpoints that are assigned to an Azure virtual machine.</span></span>

## <span data-ttu-id="c65a9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c65a9-104">SYNTAX</span></span>

```
Get-AzureEndpoint [[-Name] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c65a9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c65a9-105">DESCRIPTION</span></span>
<span data-ttu-id="c65a9-106">Cmdleten **Get-AzureEndpoint** hämtar information om slut punkterna som har tilldelats en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="c65a9-106">The **Get-AzureEndpoint** cmdlet gets information about the endpoints that are assigned to an Azure virtual machine.</span></span>

## <span data-ttu-id="c65a9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c65a9-107">EXAMPLES</span></span>

### <span data-ttu-id="c65a9-108">Exempel 1: Hämta slut punkts information för en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="c65a9-108">Example 1: Get endpoint information for a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine12" | Get-AzureEndpoint
```

<span data-ttu-id="c65a9-109">Det här kommandot hämtar konfigurationen för en virtuell dator med namnet VirtualMachine12 med hjälp av cmdleten **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="c65a9-109">This command retrieves the configuration of a virtual machine named VirtualMachine12 by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="c65a9-110">Kommandot skickar det till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="c65a9-110">The command passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c65a9-111">Denna cmdlet hämtar slut punkts information för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="c65a9-111">This cmdlet gets endpoint information for that virtual machine.</span></span>

## <span data-ttu-id="c65a9-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c65a9-112">PARAMETERS</span></span>

### <span data-ttu-id="c65a9-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c65a9-113">-InformationAction</span></span>
<span data-ttu-id="c65a9-114">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="c65a9-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c65a9-115">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="c65a9-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c65a9-116">Vidare</span><span class="sxs-lookup"><span data-stu-id="c65a9-116">Continue</span></span>
- <span data-ttu-id="c65a9-117">Över</span><span class="sxs-lookup"><span data-stu-id="c65a9-117">Ignore</span></span>
- <span data-ttu-id="c65a9-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="c65a9-118">Inquire</span></span>
- <span data-ttu-id="c65a9-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c65a9-119">SilentlyContinue</span></span>
- <span data-ttu-id="c65a9-120">Stanna</span><span class="sxs-lookup"><span data-stu-id="c65a9-120">Stop</span></span>
- <span data-ttu-id="c65a9-121">Avbryt</span><span class="sxs-lookup"><span data-stu-id="c65a9-121">Suspend</span></span>

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

### <span data-ttu-id="c65a9-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c65a9-122">-InformationVariable</span></span>
<span data-ttu-id="c65a9-123">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="c65a9-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c65a9-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="c65a9-124">-Name</span></span>
<span data-ttu-id="c65a9-125">Anger namnet på den slut punkt där denna cmdlet hämtar information.</span><span class="sxs-lookup"><span data-stu-id="c65a9-125">Specifies the name of the endpoint for which this cmdlet gets information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c65a9-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="c65a9-126">-Profile</span></span>
<span data-ttu-id="c65a9-127">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="c65a9-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c65a9-128">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="c65a9-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c65a9-129">-VM</span><span class="sxs-lookup"><span data-stu-id="c65a9-129">-VM</span></span>
<span data-ttu-id="c65a9-130">Anger den virtuella dator från vilken denna cmdlet hämtar slut punkts information.</span><span class="sxs-lookup"><span data-stu-id="c65a9-130">Specifies the virtual machine from which this cmdlet gets endpoint information.</span></span>

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

### <span data-ttu-id="c65a9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c65a9-131">CommonParameters</span></span>
<span data-ttu-id="c65a9-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c65a9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c65a9-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c65a9-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c65a9-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c65a9-134">INPUTS</span></span>

## <span data-ttu-id="c65a9-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c65a9-135">OUTPUTS</span></span>

## <span data-ttu-id="c65a9-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c65a9-136">NOTES</span></span>

## <span data-ttu-id="c65a9-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c65a9-137">RELATED LINKS</span></span>

[<span data-ttu-id="c65a9-138">Add-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="c65a9-138">Add-AzureEndpoint</span></span>](./Add-AzureEndpoint.md)

[<span data-ttu-id="c65a9-139">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="c65a9-139">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="c65a9-140">Remove-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="c65a9-140">Remove-AzureEndpoint</span></span>](./Remove-AzureEndpoint.md)

[<span data-ttu-id="c65a9-141">Set-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="c65a9-141">Set-AzureEndpoint</span></span>](./Set-AzureEndpoint.md)


