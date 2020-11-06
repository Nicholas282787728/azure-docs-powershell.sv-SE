---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 49D17667-35C3-4A79-A0C8-C197DAA5CD90
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMADDomainExtension.md
ms.openlocfilehash: 398cc4b8f23ca5296aec741eb720833f589b0e2c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575290"
---
# <span data-ttu-id="cd3cc-101">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="cd3cc-101">Get-AzureRmVMADDomainExtension</span></span>

## <span data-ttu-id="cd3cc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cd3cc-102">SYNOPSIS</span></span>
<span data-ttu-id="cd3cc-103">Hämtar information om ett AD-domännätverk.</span><span class="sxs-lookup"><span data-stu-id="cd3cc-103">Gets information about an AD domain extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd3cc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cd3cc-104">SYNTAX</span></span>

```
Get-AzureRmVMADDomainExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd3cc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cd3cc-105">DESCRIPTION</span></span>
<span data-ttu-id="cd3cc-106">Cmdleten **Get-AzureRmVMADDomainExtension** hämtar information om den angivna Azure Active Directory (AD)-domän tillägget.</span><span class="sxs-lookup"><span data-stu-id="cd3cc-106">The **Get-AzureRmVMADDomainExtension** cmdlet gets information about the specified Azure Active Directory (AD) domain extension.</span></span>

## <span data-ttu-id="cd3cc-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cd3cc-107">EXAMPLES</span></span>

## <span data-ttu-id="cd3cc-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cd3cc-108">PARAMETERS</span></span>

### <span data-ttu-id="cd3cc-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd3cc-109">-DefaultProfile</span></span>
<span data-ttu-id="cd3cc-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cd3cc-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd3cc-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="cd3cc-111">-Name</span></span>
<span data-ttu-id="cd3cc-112">Anger namnet på domän tillägget.</span><span class="sxs-lookup"><span data-stu-id="cd3cc-112">Specifies the name of the domain extension.</span></span>

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

### <span data-ttu-id="cd3cc-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd3cc-113">-ResourceGroupName</span></span>
<span data-ttu-id="cd3cc-114">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="cd3cc-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="cd3cc-115">-Status</span><span class="sxs-lookup"><span data-stu-id="cd3cc-115">-Status</span></span>
<span data-ttu-id="cd3cc-116">Anger att denna cmdlet hämtar instans-vyn för domän tillägget.</span><span class="sxs-lookup"><span data-stu-id="cd3cc-116">Indicates that this cmdlet gets the instance view of the domain extension.</span></span>

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

### <span data-ttu-id="cd3cc-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="cd3cc-117">-VMName</span></span>
<span data-ttu-id="cd3cc-118">Anger namnet på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="cd3cc-118">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="cd3cc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd3cc-119">CommonParameters</span></span>
<span data-ttu-id="cd3cc-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd3cc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd3cc-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd3cc-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd3cc-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cd3cc-122">INPUTS</span></span>

### <span data-ttu-id="cd3cc-123">System. String</span><span class="sxs-lookup"><span data-stu-id="cd3cc-123">System.String</span></span>

### <span data-ttu-id="cd3cc-124">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="cd3cc-124">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="cd3cc-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cd3cc-125">OUTPUTS</span></span>

### <span data-ttu-id="cd3cc-126">Microsoft. Azure. commands. Compute. Models. VirtualMachineADDomainExtensionContext</span><span class="sxs-lookup"><span data-stu-id="cd3cc-126">Microsoft.Azure.Commands.Compute.Models.VirtualMachineADDomainExtensionContext</span></span>

## <span data-ttu-id="cd3cc-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cd3cc-127">NOTES</span></span>

## <span data-ttu-id="cd3cc-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cd3cc-128">RELATED LINKS</span></span>

[<span data-ttu-id="cd3cc-129">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="cd3cc-129">Set-AzureRmVMADDomainExtension</span></span>](./Set-AzureRmVMADDomainExtension.md)


