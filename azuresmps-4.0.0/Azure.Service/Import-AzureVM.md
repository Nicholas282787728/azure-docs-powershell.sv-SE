---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7180CAC6-BFC1-4A18-A754-83D5F05C5BEF
online version: ''
schema: 2.0.0
ms.openlocfilehash: c62c30558147bccd9cdecc73925b7e1a379d1c5b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099485"
---
# <span data-ttu-id="6183e-101">Import-AzureVM</span><span class="sxs-lookup"><span data-stu-id="6183e-101">Import-AzureVM</span></span>

## <span data-ttu-id="6183e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6183e-102">SYNOPSIS</span></span>
<span data-ttu-id="6183e-103">Importerar tillstånd från en Azure-dator från en fil.</span><span class="sxs-lookup"><span data-stu-id="6183e-103">Imports an Azure virtual machine state from a file.</span></span>

## <span data-ttu-id="6183e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6183e-104">SYNTAX</span></span>

```
Import-AzureVM [-Path] <String> [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="6183e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6183e-105">DESCRIPTION</span></span>
<span data-ttu-id="6183e-106">Cmdleten **import-AzureVM** importerar det tidigare sparade tillståndet för en virtuell dator från en XML-fil.</span><span class="sxs-lookup"><span data-stu-id="6183e-106">The **Import-AzureVM** cmdlet imports the previously saved state of a virtual machine from an XML file.</span></span>
<span data-ttu-id="6183e-107">Denna cmdlet är användbar när du senare vill skapa en virtuell dator från importerade data.</span><span class="sxs-lookup"><span data-stu-id="6183e-107">This cmdlet is useful when you want to subsequently create a virtual machine from the imported data.</span></span>

<span data-ttu-id="6183e-108">Om du kör **Exportera-AzureVM** följt av **Remove-AzureVM** och sedan **import-AzureVM** för att återskapa en virtuell dator kan det orsaka att den resulterande virtuella datorn har en annan IP-adress än den ursprungliga.</span><span class="sxs-lookup"><span data-stu-id="6183e-108">Running **Export-AzureVM** , followed by **Remove-AzureVM** and then **Import-AzureVM** to recreate a virtual machine can cause the resultant virtual machine to have a different IP address than the original.</span></span>

## <span data-ttu-id="6183e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6183e-109">EXAMPLES</span></span>

### <span data-ttu-id="6183e-110">Exempel 1: importera en tillstånds status</span><span class="sxs-lookup"><span data-stu-id="6183e-110">Example 1: Import a virtual machine state</span></span>
```
PS C:\> Import-AzureVM -Path "C:\VMstate.xml" | New-AzureVM -ServiceName "ContosoService02"
```

<span data-ttu-id="6183e-111">Det här kommandot importerar tillståndet för en virtuell dator från VMstate.xml-filen och skapar sedan en virtuell dator i den angivna moln tjänsten.</span><span class="sxs-lookup"><span data-stu-id="6183e-111">This command imports the state of a virtual machine from the VMstate.xml file, and then creates a virtual machine in the specified cloud service.</span></span>

## <span data-ttu-id="6183e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6183e-112">PARAMETERS</span></span>

### <span data-ttu-id="6183e-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="6183e-113">-InformationAction</span></span>
<span data-ttu-id="6183e-114">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="6183e-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6183e-115">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="6183e-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6183e-116">Vidare</span><span class="sxs-lookup"><span data-stu-id="6183e-116">Continue</span></span>
- <span data-ttu-id="6183e-117">Över</span><span class="sxs-lookup"><span data-stu-id="6183e-117">Ignore</span></span>
- <span data-ttu-id="6183e-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="6183e-118">Inquire</span></span>
- <span data-ttu-id="6183e-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6183e-119">SilentlyContinue</span></span>
- <span data-ttu-id="6183e-120">Stanna</span><span class="sxs-lookup"><span data-stu-id="6183e-120">Stop</span></span>
- <span data-ttu-id="6183e-121">Avbryt</span><span class="sxs-lookup"><span data-stu-id="6183e-121">Suspend</span></span>

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

### <span data-ttu-id="6183e-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6183e-122">-InformationVariable</span></span>
<span data-ttu-id="6183e-123">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="6183e-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="6183e-124">-Path</span><span class="sxs-lookup"><span data-stu-id="6183e-124">-Path</span></span>
<span data-ttu-id="6183e-125">Anger sökvägen till filen med den tidigare sparade virtuella dator statusen.</span><span class="sxs-lookup"><span data-stu-id="6183e-125">Specifies the path of the file with the previously saved virtual machine state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6183e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6183e-126">CommonParameters</span></span>
<span data-ttu-id="6183e-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6183e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6183e-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6183e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6183e-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6183e-129">INPUTS</span></span>

## <span data-ttu-id="6183e-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6183e-130">OUTPUTS</span></span>

## <span data-ttu-id="6183e-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6183e-131">NOTES</span></span>

## <span data-ttu-id="6183e-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6183e-132">RELATED LINKS</span></span>

[<span data-ttu-id="6183e-133">Exportera-AzureVM</span><span class="sxs-lookup"><span data-stu-id="6183e-133">Export-AzureVM</span></span>](./Export-AzureVM.md)

[<span data-ttu-id="6183e-134">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="6183e-134">New-AzureVM</span></span>](./New-AzureVM.md)


