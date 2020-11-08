---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: ACBE32E5-AA8C-43CA-9FF4-4B59906C6B85
online version: ''
schema: 2.0.0
ms.openlocfilehash: 45d18179fba41d39456a11575fc2041ad4be8557
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099760"
---
# <span data-ttu-id="13e59-101">Get-AzureVMImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="13e59-101">Get-AzureVMImageDiskConfigSet</span></span>

## <span data-ttu-id="13e59-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="13e59-102">SYNOPSIS</span></span>
<span data-ttu-id="13e59-103">Hämtar ett objekt från en uppsättning med indata från indatabilden.</span><span class="sxs-lookup"><span data-stu-id="13e59-103">Gets a disk configuration set object from the input image context.</span></span>

## <span data-ttu-id="13e59-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="13e59-104">SYNTAX</span></span>

```
Get-AzureVMImageDiskConfigSet [[-ImageContext] <OSImageContext>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="13e59-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="13e59-105">DESCRIPTION</span></span>
<span data-ttu-id="13e59-106">Cmdleten **Get-AzureVMImageDiskConfigSet** hämtar ett objekt för disk konfigurations uppsättning från den angivna bild kontexten.</span><span class="sxs-lookup"><span data-stu-id="13e59-106">The **Get-AzureVMImageDiskConfigSet** cmdlet gets a disk configuration set object from the input image context.</span></span>

## <span data-ttu-id="13e59-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="13e59-107">EXAMPLES</span></span>

### <span data-ttu-id="13e59-108">Exempel 1: Hämta ett objekt för disk konfiguration från en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="13e59-108">Example 1: Get a disk configuration set object from a virtual machine</span></span>
```
PS C:\> Get-AzureVMImage -ImageName $Img | Get-AzureVMImageDiskConfigSet
```

<span data-ttu-id="13e59-109">Med det här kommandot får du ett objekt från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="13e59-109">This command gets a disk configuration set object from a virtual machine.</span></span>

## <span data-ttu-id="13e59-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="13e59-110">PARAMETERS</span></span>

### <span data-ttu-id="13e59-111">-ImageContext</span><span class="sxs-lookup"><span data-stu-id="13e59-111">-ImageContext</span></span>
<span data-ttu-id="13e59-112">Anger bild kontext för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="13e59-112">Specifies the virtual machine image context.</span></span>

```yaml
Type: OSImageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13e59-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="13e59-113">-InformationAction</span></span>
<span data-ttu-id="13e59-114">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="13e59-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="13e59-115">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="13e59-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="13e59-116">Vidare</span><span class="sxs-lookup"><span data-stu-id="13e59-116">Continue</span></span>
- <span data-ttu-id="13e59-117">Över</span><span class="sxs-lookup"><span data-stu-id="13e59-117">Ignore</span></span>
- <span data-ttu-id="13e59-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="13e59-118">Inquire</span></span>
- <span data-ttu-id="13e59-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="13e59-119">SilentlyContinue</span></span>
- <span data-ttu-id="13e59-120">Stanna</span><span class="sxs-lookup"><span data-stu-id="13e59-120">Stop</span></span>
- <span data-ttu-id="13e59-121">Avbryt</span><span class="sxs-lookup"><span data-stu-id="13e59-121">Suspend</span></span>

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

### <span data-ttu-id="13e59-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="13e59-122">-InformationVariable</span></span>
<span data-ttu-id="13e59-123">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="13e59-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="13e59-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13e59-124">CommonParameters</span></span>
<span data-ttu-id="13e59-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13e59-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13e59-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13e59-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13e59-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="13e59-127">INPUTS</span></span>

## <span data-ttu-id="13e59-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="13e59-128">OUTPUTS</span></span>

### <span data-ttu-id="13e59-129">Microsoft. WindowsAzure. kommandon. ServiceManagement. Model. VirtualMachineImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="13e59-129">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="13e59-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="13e59-130">NOTES</span></span>

## <span data-ttu-id="13e59-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="13e59-131">RELATED LINKS</span></span>

[<span data-ttu-id="13e59-132">New-AzureVMImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="13e59-132">New-AzureVMImageDiskConfigSet</span></span>](./New-AzureVMImageDiskConfigSet.md)

[<span data-ttu-id="13e59-133">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="13e59-133">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)


