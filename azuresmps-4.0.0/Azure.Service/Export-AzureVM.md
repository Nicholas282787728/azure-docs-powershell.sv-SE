---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 78099E89-63C9-4019-A4ED-EF37D2383A09
online version: ''
schema: 2.0.0
ms.openlocfilehash: 23e6165e50c227320875fa70e97d63b0cdd78781
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093403"
---
# <span data-ttu-id="fff90-101">Export-AzureVM</span><span class="sxs-lookup"><span data-stu-id="fff90-101">Export-AzureVM</span></span>

## <span data-ttu-id="fff90-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fff90-102">SYNOPSIS</span></span>
<span data-ttu-id="fff90-103">Exporterar en tillstånds status till en fil.</span><span class="sxs-lookup"><span data-stu-id="fff90-103">Exports an Azure virtual machine state to a file.</span></span>

## <span data-ttu-id="fff90-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fff90-104">SYNTAX</span></span>

```
Export-AzureVM [-ServiceName] <String> [-Name] <String> [-Path] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="fff90-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fff90-105">DESCRIPTION</span></span>
<span data-ttu-id="fff90-106">Cmdleten **export-AzureVM** exporterar statusen för en virtuell dator till en XML-fil.</span><span class="sxs-lookup"><span data-stu-id="fff90-106">The **Export-AzureVM** cmdlet exports the state of a virtual machine to an .xml file.</span></span>

<span data-ttu-id="fff90-107">Om du kör **Exportera-AzureVM** följt av **Remove-AzureVM** och sedan **import-AzureVM** för att återskapa en virtuell dator kan det orsaka att den resulterande virtuella datorn har en annan IP-adress än den ursprungliga.</span><span class="sxs-lookup"><span data-stu-id="fff90-107">Running **Export-AzureVM** , followed by **Remove-AzureVM** and then **Import-AzureVM** to recreate a virtual machine can cause the resultant virtual machine to have a different IP address than the original.</span></span>

## <span data-ttu-id="fff90-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fff90-108">EXAMPLES</span></span>

### <span data-ttu-id="fff90-109">Exempel 1: exportera en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="fff90-109">Example 1: Export a virtual machine</span></span>
```
PS C:\> Export-AzureVM -ServiceName "ContosoService" -Name "ContosoRole06" -Path "C:\vms\VMstate.xml"
```

<span data-ttu-id="fff90-110">Det här kommandot exporterar statusen för den virtuella datorn till VMstate.xml-filen.</span><span class="sxs-lookup"><span data-stu-id="fff90-110">This command exports the state of the specified virtual machine to the VMstate.xml file.</span></span>

## <span data-ttu-id="fff90-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fff90-111">PARAMETERS</span></span>

### <span data-ttu-id="fff90-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="fff90-112">-InformationAction</span></span>
<span data-ttu-id="fff90-113">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="fff90-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="fff90-114">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="fff90-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fff90-115">Vidare</span><span class="sxs-lookup"><span data-stu-id="fff90-115">Continue</span></span>
- <span data-ttu-id="fff90-116">Över</span><span class="sxs-lookup"><span data-stu-id="fff90-116">Ignore</span></span>
- <span data-ttu-id="fff90-117">Inquire</span><span class="sxs-lookup"><span data-stu-id="fff90-117">Inquire</span></span>
- <span data-ttu-id="fff90-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="fff90-118">SilentlyContinue</span></span>
- <span data-ttu-id="fff90-119">Stanna</span><span class="sxs-lookup"><span data-stu-id="fff90-119">Stop</span></span>
- <span data-ttu-id="fff90-120">Avbryt</span><span class="sxs-lookup"><span data-stu-id="fff90-120">Suspend</span></span>

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

### <span data-ttu-id="fff90-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="fff90-121">-InformationVariable</span></span>
<span data-ttu-id="fff90-122">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="fff90-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="fff90-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="fff90-123">-Name</span></span>
<span data-ttu-id="fff90-124">Anger namnet på den virtuella dator för vilken denna cmdlet exporterar status.</span><span class="sxs-lookup"><span data-stu-id="fff90-124">Specifies the name of the virtual machine for which this cmdlet exports state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fff90-125">-Path</span><span class="sxs-lookup"><span data-stu-id="fff90-125">-Path</span></span>
<span data-ttu-id="fff90-126">Anger sökvägen och fil namnet som denna cmdlet sparar den virtuella datorns tillstånd i.</span><span class="sxs-lookup"><span data-stu-id="fff90-126">Specifies the path and file name to which this cmdlet saves the virtual machine state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fff90-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="fff90-127">-Profile</span></span>
<span data-ttu-id="fff90-128">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="fff90-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fff90-129">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="fff90-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fff90-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="fff90-130">-ServiceName</span></span>
<span data-ttu-id="fff90-131">Anger namnet på den Azure-tjänst som är värd för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="fff90-131">Specifies the name of the Azure service that hosts the virtual machine.</span></span>

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

### <span data-ttu-id="fff90-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fff90-132">CommonParameters</span></span>
<span data-ttu-id="fff90-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fff90-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fff90-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fff90-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fff90-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fff90-135">INPUTS</span></span>

## <span data-ttu-id="fff90-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fff90-136">OUTPUTS</span></span>

## <span data-ttu-id="fff90-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fff90-137">NOTES</span></span>

## <span data-ttu-id="fff90-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fff90-138">RELATED LINKS</span></span>

[<span data-ttu-id="fff90-139">Import-AzureVM</span><span class="sxs-lookup"><span data-stu-id="fff90-139">Import-AzureVM</span></span>](./Import-AzureVM.md)


