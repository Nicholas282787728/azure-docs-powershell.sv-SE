---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 49D17667-35C3-4A79-A0C8-C197DAA5CD90
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMADDomainExtension.md
ms.openlocfilehash: e4431b657c72a82f1316f5eb8b74f45fac0f04aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575004"
---
# <span data-ttu-id="05f34-101">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="05f34-101">Get-AzureRmVMADDomainExtension</span></span>

## <span data-ttu-id="05f34-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="05f34-102">SYNOPSIS</span></span>
<span data-ttu-id="05f34-103">Hämtar information om ett AD-domännätverk.</span><span class="sxs-lookup"><span data-stu-id="05f34-103">Gets information about an AD domain extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05f34-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="05f34-104">SYNTAX</span></span>

```
Get-AzureRmVMADDomainExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05f34-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="05f34-105">DESCRIPTION</span></span>
<span data-ttu-id="05f34-106">Cmdleten **Get-AzureRmVMADDomainExtension** hämtar information om den angivna Azure Active Directory (AD)-domän tillägget.</span><span class="sxs-lookup"><span data-stu-id="05f34-106">The **Get-AzureRmVMADDomainExtension** cmdlet gets information about the specified Azure Active Directory (AD) domain extension.</span></span>

## <span data-ttu-id="05f34-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="05f34-107">EXAMPLES</span></span>

## <span data-ttu-id="05f34-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="05f34-108">PARAMETERS</span></span>

### <span data-ttu-id="05f34-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05f34-109">-DefaultProfile</span></span>
<span data-ttu-id="05f34-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="05f34-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05f34-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="05f34-111">-Name</span></span>
<span data-ttu-id="05f34-112">Anger namnet på domän tillägget.</span><span class="sxs-lookup"><span data-stu-id="05f34-112">Specifies the name of the domain extension.</span></span>

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

### <span data-ttu-id="05f34-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05f34-113">-ResourceGroupName</span></span>
<span data-ttu-id="05f34-114">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="05f34-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="05f34-115">-Status</span><span class="sxs-lookup"><span data-stu-id="05f34-115">-Status</span></span>
<span data-ttu-id="05f34-116">Anger att denna cmdlet hämtar instans-vyn för domän tillägget.</span><span class="sxs-lookup"><span data-stu-id="05f34-116">Indicates that this cmdlet gets the instance view of the domain extension.</span></span>

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

### <span data-ttu-id="05f34-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="05f34-117">-VMName</span></span>
<span data-ttu-id="05f34-118">Anger namnet på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="05f34-118">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="05f34-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05f34-119">CommonParameters</span></span>
<span data-ttu-id="05f34-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05f34-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05f34-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05f34-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05f34-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="05f34-122">INPUTS</span></span>

## <span data-ttu-id="05f34-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="05f34-123">OUTPUTS</span></span>

## <span data-ttu-id="05f34-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="05f34-124">NOTES</span></span>

## <span data-ttu-id="05f34-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="05f34-125">RELATED LINKS</span></span>

[<span data-ttu-id="05f34-126">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="05f34-126">Set-AzureRmVMADDomainExtension</span></span>](./Set-AzureRmVMADDomainExtension.md)


