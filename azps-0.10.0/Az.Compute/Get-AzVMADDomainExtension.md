---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 49D17667-35C3-4A79-A0C8-C197DAA5CD90
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMADDomainExtension.md
ms.openlocfilehash: 809246520c4e6b07a1aca406ef3ec17eb9df31f1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93925213"
---
# <span data-ttu-id="f35ea-101">Get-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="f35ea-101">Get-AzVMADDomainExtension</span></span>

## <span data-ttu-id="f35ea-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f35ea-102">SYNOPSIS</span></span>
<span data-ttu-id="f35ea-103">Hämtar information om ett AD-domännätverk.</span><span class="sxs-lookup"><span data-stu-id="f35ea-103">Gets information about an AD domain extension.</span></span>

## <span data-ttu-id="f35ea-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f35ea-104">SYNTAX</span></span>

```
Get-AzVMADDomainExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f35ea-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f35ea-105">DESCRIPTION</span></span>
<span data-ttu-id="f35ea-106">Cmdleten **Get-AzVMADDomainExtension** hämtar information om den angivna Azure Active Directory (AD)-domän tillägget.</span><span class="sxs-lookup"><span data-stu-id="f35ea-106">The **Get-AzVMADDomainExtension** cmdlet gets information about the specified Azure Active Directory (AD) domain extension.</span></span>

## <span data-ttu-id="f35ea-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f35ea-107">EXAMPLES</span></span>

### <span data-ttu-id="f35ea-108">9.1</span><span class="sxs-lookup"><span data-stu-id="f35ea-108">1:</span></span>
```

```

## <span data-ttu-id="f35ea-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f35ea-109">PARAMETERS</span></span>

### <span data-ttu-id="f35ea-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f35ea-110">-DefaultProfile</span></span>
<span data-ttu-id="f35ea-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f35ea-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f35ea-112">-Namn</span><span class="sxs-lookup"><span data-stu-id="f35ea-112">-Name</span></span>
<span data-ttu-id="f35ea-113">Anger namnet på domän tillägget.</span><span class="sxs-lookup"><span data-stu-id="f35ea-113">Specifies the name of the domain extension.</span></span>

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

### <span data-ttu-id="f35ea-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f35ea-114">-ResourceGroupName</span></span>
<span data-ttu-id="f35ea-115">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="f35ea-115">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f35ea-116">-Status</span><span class="sxs-lookup"><span data-stu-id="f35ea-116">-Status</span></span>
<span data-ttu-id="f35ea-117">Anger att denna cmdlet hämtar instans-vyn för domän tillägget.</span><span class="sxs-lookup"><span data-stu-id="f35ea-117">Indicates that this cmdlet gets the instance view of the domain extension.</span></span>

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

### <span data-ttu-id="f35ea-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="f35ea-118">-VMName</span></span>
<span data-ttu-id="f35ea-119">Anger namnet på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="f35ea-119">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="f35ea-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f35ea-120">CommonParameters</span></span>
<span data-ttu-id="f35ea-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f35ea-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f35ea-122">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f35ea-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f35ea-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f35ea-123">INPUTS</span></span>

### <span data-ttu-id="f35ea-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="f35ea-124">None</span></span>
<span data-ttu-id="f35ea-125">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="f35ea-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f35ea-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f35ea-126">OUTPUTS</span></span>

### <span data-ttu-id="f35ea-127">Microsoft. Azure. commands. Compute. Models. VirtualMachineADDomainExtensionContext</span><span class="sxs-lookup"><span data-stu-id="f35ea-127">Microsoft.Azure.Commands.Compute.Models.VirtualMachineADDomainExtensionContext</span></span>

## <span data-ttu-id="f35ea-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f35ea-128">NOTES</span></span>

## <span data-ttu-id="f35ea-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f35ea-129">RELATED LINKS</span></span>

[<span data-ttu-id="f35ea-130">Set-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="f35ea-130">Set-AzVMADDomainExtension</span></span>](./Set-AzVMADDomainExtension.md)


