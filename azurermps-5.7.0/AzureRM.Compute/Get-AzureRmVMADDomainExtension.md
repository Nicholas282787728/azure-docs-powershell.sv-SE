---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 49D17667-35C3-4A79-A0C8-C197DAA5CD90
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMADDomainExtension.md
ms.openlocfilehash: d55d84560ca75a508a05276d8d33eb78d1d50ab5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578307"
---
# <span data-ttu-id="9217e-101">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="9217e-101">Get-AzureRmVMADDomainExtension</span></span>

## <span data-ttu-id="9217e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9217e-102">SYNOPSIS</span></span>
<span data-ttu-id="9217e-103">Hämtar information om ett AD-domännätverk.</span><span class="sxs-lookup"><span data-stu-id="9217e-103">Gets information about an AD domain extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9217e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9217e-104">SYNTAX</span></span>

```
Get-AzureRmVMADDomainExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [<CommonParameters>]
```

## <span data-ttu-id="9217e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9217e-105">DESCRIPTION</span></span>
<span data-ttu-id="9217e-106">Cmdleten **Get-AzureRmVMADDomainExtension** hämtar information om den angivna Azure Active Directory (AD)-domän tillägget.</span><span class="sxs-lookup"><span data-stu-id="9217e-106">The **Get-AzureRmVMADDomainExtension** cmdlet gets information about the specified Azure Active Directory (AD) domain extension.</span></span>

## <span data-ttu-id="9217e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9217e-107">EXAMPLES</span></span>

## <span data-ttu-id="9217e-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9217e-108">PARAMETERS</span></span>

### <span data-ttu-id="9217e-109">-Namn</span><span class="sxs-lookup"><span data-stu-id="9217e-109">-Name</span></span>
<span data-ttu-id="9217e-110">Anger namnet på domän tillägget.</span><span class="sxs-lookup"><span data-stu-id="9217e-110">Specifies the name of the domain extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9217e-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9217e-111">-ResourceGroupName</span></span>
<span data-ttu-id="9217e-112">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="9217e-112">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="9217e-113">-Status</span><span class="sxs-lookup"><span data-stu-id="9217e-113">-Status</span></span>
<span data-ttu-id="9217e-114">Anger att denna cmdlet hämtar instans-vyn för domän tillägget.</span><span class="sxs-lookup"><span data-stu-id="9217e-114">Indicates that this cmdlet gets the instance view of the domain extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9217e-115">-VMName</span><span class="sxs-lookup"><span data-stu-id="9217e-115">-VMName</span></span>
<span data-ttu-id="9217e-116">Anger namnet på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="9217e-116">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9217e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9217e-117">CommonParameters</span></span>
<span data-ttu-id="9217e-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9217e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9217e-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9217e-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9217e-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9217e-120">INPUTS</span></span>

### <span data-ttu-id="9217e-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="9217e-121">None</span></span>
<span data-ttu-id="9217e-122">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="9217e-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9217e-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9217e-123">OUTPUTS</span></span>

## <span data-ttu-id="9217e-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9217e-124">NOTES</span></span>

## <span data-ttu-id="9217e-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9217e-125">RELATED LINKS</span></span>

[<span data-ttu-id="9217e-126">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="9217e-126">Set-AzureRmVMADDomainExtension</span></span>](./Set-AzureRmVMADDomainExtension.md)


