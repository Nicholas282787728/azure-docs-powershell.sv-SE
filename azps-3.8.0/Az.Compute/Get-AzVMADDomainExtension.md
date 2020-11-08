---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 49D17667-35C3-4A79-A0C8-C197DAA5CD90
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMADDomainExtension.md
ms.openlocfilehash: ca6b3d4863629aa94585db9850042fff4165dd10
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092792"
---
# <span data-ttu-id="56bf9-101">Get-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="56bf9-101">Get-AzVMADDomainExtension</span></span>

## <span data-ttu-id="56bf9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="56bf9-102">SYNOPSIS</span></span>
<span data-ttu-id="56bf9-103">Hämtar information om ett AD-domännätverk.</span><span class="sxs-lookup"><span data-stu-id="56bf9-103">Gets information about an AD domain extension.</span></span>

## <span data-ttu-id="56bf9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="56bf9-104">SYNTAX</span></span>

```
Get-AzVMADDomainExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56bf9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="56bf9-105">DESCRIPTION</span></span>
<span data-ttu-id="56bf9-106">Cmdleten **Get-AzVMADDomainExtension** hämtar information om den angivna Azure Active Directory (AD)-domän tillägget.</span><span class="sxs-lookup"><span data-stu-id="56bf9-106">The **Get-AzVMADDomainExtension** cmdlet gets information about the specified Azure Active Directory (AD) domain extension.</span></span>

## <span data-ttu-id="56bf9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="56bf9-107">EXAMPLES</span></span>

## <span data-ttu-id="56bf9-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="56bf9-108">PARAMETERS</span></span>

### <span data-ttu-id="56bf9-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56bf9-109">-DefaultProfile</span></span>
<span data-ttu-id="56bf9-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="56bf9-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56bf9-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="56bf9-111">-Name</span></span>
<span data-ttu-id="56bf9-112">Anger namnet på domän tillägget.</span><span class="sxs-lookup"><span data-stu-id="56bf9-112">Specifies the name of the domain extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56bf9-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56bf9-113">-ResourceGroupName</span></span>
<span data-ttu-id="56bf9-114">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="56bf9-114">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56bf9-115">-Status</span><span class="sxs-lookup"><span data-stu-id="56bf9-115">-Status</span></span>
<span data-ttu-id="56bf9-116">Anger att denna cmdlet hämtar instans-vyn för domän tillägget.</span><span class="sxs-lookup"><span data-stu-id="56bf9-116">Indicates that this cmdlet gets the instance view of the domain extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56bf9-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="56bf9-117">-VMName</span></span>
<span data-ttu-id="56bf9-118">Anger namnet på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="56bf9-118">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56bf9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56bf9-119">CommonParameters</span></span>
<span data-ttu-id="56bf9-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56bf9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56bf9-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="56bf9-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56bf9-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="56bf9-122">INPUTS</span></span>

### <span data-ttu-id="56bf9-123">System. String</span><span class="sxs-lookup"><span data-stu-id="56bf9-123">System.String</span></span>

### <span data-ttu-id="56bf9-124">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="56bf9-124">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="56bf9-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="56bf9-125">OUTPUTS</span></span>

### <span data-ttu-id="56bf9-126">Microsoft. Azure. commands. Compute. Models. VirtualMachineADDomainExtensionContext</span><span class="sxs-lookup"><span data-stu-id="56bf9-126">Microsoft.Azure.Commands.Compute.Models.VirtualMachineADDomainExtensionContext</span></span>

## <span data-ttu-id="56bf9-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="56bf9-127">NOTES</span></span>

## <span data-ttu-id="56bf9-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="56bf9-128">RELATED LINKS</span></span>

[<span data-ttu-id="56bf9-129">Set-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="56bf9-129">Set-AzVMADDomainExtension</span></span>](./Set-AzVMADDomainExtension.md)


