---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmDefault.md
ms.openlocfilehash: 7430402d62d88ea192b94166f48c0657e47cbf15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755468"
---
# <span data-ttu-id="b6275-101">Get-AzureRmDefault</span><span class="sxs-lookup"><span data-stu-id="b6275-101">Get-AzureRmDefault</span></span>

## <span data-ttu-id="b6275-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b6275-102">SYNOPSIS</span></span>
<span data-ttu-id="b6275-103">Hämta de standardvärden som användaren angett i den aktuella kontexten.</span><span class="sxs-lookup"><span data-stu-id="b6275-103">Get the defaults set by the user in the current context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6275-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b6275-104">SYNTAX</span></span>

```
Get-AzureRmDefault [-ResourceGroup] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6275-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b6275-105">DESCRIPTION</span></span>
<span data-ttu-id="b6275-106">Get-AzureRmDefault cmdlet får resurs gruppen att användaren har angett som standard i den aktuella kontexten.</span><span class="sxs-lookup"><span data-stu-id="b6275-106">The Get-AzureRmDefault cmdlet gets the Resource Group that the user has set as default in the current context.</span></span>

## <span data-ttu-id="b6275-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b6275-107">EXAMPLES</span></span>

### <span data-ttu-id="b6275-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b6275-108">Example 1</span></span>
```
PS C:\> Get-AzureRmDefault

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="b6275-109">Det här kommandot returnerar de aktuella standardinställningarna om det finns standardinställningar eller om inget standardvärde anges.</span><span class="sxs-lookup"><span data-stu-id="b6275-109">This command returns the current defaults if there are defaults set, or returns nothing if no default is set.</span></span>

### <span data-ttu-id="b6275-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="b6275-110">Example 2</span></span>
```
PS C:\> Get-AzureRmDefault -ResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="b6275-111">Det här kommandot returnerar den aktuella standard resurs gruppen om det finns en standard uppsättning eller om inget standardvärde har angetts.</span><span class="sxs-lookup"><span data-stu-id="b6275-111">This command returns the current default Resource Group if there is a default set, or returns nothing if no default is set.</span></span>

## <span data-ttu-id="b6275-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b6275-112">PARAMETERS</span></span>

### <span data-ttu-id="b6275-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6275-113">-DefaultProfile</span></span>
<span data-ttu-id="b6275-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b6275-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6275-115">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b6275-115">-ResourceGroup</span></span>
<span data-ttu-id="b6275-116">Visa standard resurs grupp</span><span class="sxs-lookup"><span data-stu-id="b6275-116">Display Default Resource Group</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6275-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6275-117">CommonParameters</span></span>
<span data-ttu-id="b6275-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6275-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6275-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6275-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6275-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b6275-120">INPUTS</span></span>

### <span data-ttu-id="b6275-121">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b6275-121">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b6275-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b6275-122">OUTPUTS</span></span>

### <span data-ttu-id="b6275-123">Microsoft. Azure. commands. Profile. Models. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b6275-123">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span></span>

## <span data-ttu-id="b6275-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b6275-124">NOTES</span></span>

## <span data-ttu-id="b6275-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b6275-125">RELATED LINKS</span></span>
