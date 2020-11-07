---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 49D17667-35C3-4A79-A0C8-C197DAA5CD90
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmaddomainextension
schema: 2.0.0
ms.openlocfilehash: 01a5a69053cfd05186abae45d5b53fff0b022b98
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929481"
---
# <span data-ttu-id="f9a23-101">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="f9a23-101">Get-AzureRmVMADDomainExtension</span></span>

## <span data-ttu-id="f9a23-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f9a23-102">SYNOPSIS</span></span>
<span data-ttu-id="f9a23-103">Hämtar information om ett AD-domännätverk.</span><span class="sxs-lookup"><span data-stu-id="f9a23-103">Gets information about an AD domain extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9a23-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f9a23-104">SYNTAX</span></span>

```
Get-AzureRmVMADDomainExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9a23-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f9a23-105">DESCRIPTION</span></span>
<span data-ttu-id="f9a23-106">Cmdleten **Get-AzureRmVMADDomainExtension** hämtar information om den angivna Azure Active Directory (AD)-domän tillägget.</span><span class="sxs-lookup"><span data-stu-id="f9a23-106">The **Get-AzureRmVMADDomainExtension** cmdlet gets information about the specified Azure Active Directory (AD) domain extension.</span></span>

## <span data-ttu-id="f9a23-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f9a23-107">EXAMPLES</span></span>

### <span data-ttu-id="f9a23-108">9.1</span><span class="sxs-lookup"><span data-stu-id="f9a23-108">1:</span></span>
```

```

## <span data-ttu-id="f9a23-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f9a23-109">PARAMETERS</span></span>

### <span data-ttu-id="f9a23-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9a23-110">-DefaultProfile</span></span>
<span data-ttu-id="f9a23-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f9a23-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9a23-112">-Namn</span><span class="sxs-lookup"><span data-stu-id="f9a23-112">-Name</span></span>
<span data-ttu-id="f9a23-113">Anger namnet på domän tillägget.</span><span class="sxs-lookup"><span data-stu-id="f9a23-113">Specifies the name of the domain extension.</span></span>

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

### <span data-ttu-id="f9a23-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9a23-114">-ResourceGroupName</span></span>
<span data-ttu-id="f9a23-115">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="f9a23-115">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f9a23-116">-Status</span><span class="sxs-lookup"><span data-stu-id="f9a23-116">-Status</span></span>
<span data-ttu-id="f9a23-117">Anger att denna cmdlet hämtar instans-vyn för domän tillägget.</span><span class="sxs-lookup"><span data-stu-id="f9a23-117">Indicates that this cmdlet gets the instance view of the domain extension.</span></span>

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

### <span data-ttu-id="f9a23-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="f9a23-118">-VMName</span></span>
<span data-ttu-id="f9a23-119">Anger namnet på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="f9a23-119">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="f9a23-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9a23-120">CommonParameters</span></span>
<span data-ttu-id="f9a23-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9a23-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9a23-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9a23-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9a23-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f9a23-123">INPUTS</span></span>

### <span data-ttu-id="f9a23-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="f9a23-124">None</span></span>
<span data-ttu-id="f9a23-125">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="f9a23-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f9a23-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f9a23-126">OUTPUTS</span></span>

### <span data-ttu-id="f9a23-127">Microsoft. Azure. commands. Compute. Models. VirtualMachineADDomainExtensionContext</span><span class="sxs-lookup"><span data-stu-id="f9a23-127">Microsoft.Azure.Commands.Compute.Models.VirtualMachineADDomainExtensionContext</span></span>

## <span data-ttu-id="f9a23-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f9a23-128">NOTES</span></span>

## <span data-ttu-id="f9a23-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f9a23-129">RELATED LINKS</span></span>

[<span data-ttu-id="f9a23-130">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="f9a23-130">Set-AzureRmVMADDomainExtension</span></span>](./Set-AzureRmVMADDomainExtension.md)


