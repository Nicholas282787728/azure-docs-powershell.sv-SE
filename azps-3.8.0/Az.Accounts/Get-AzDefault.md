---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzDefault.md
ms.openlocfilehash: 43806326f572030997299353cfc7e79e5587a4ab
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090747"
---
# <span data-ttu-id="ca8e1-101">Get-AzDefault</span><span class="sxs-lookup"><span data-stu-id="ca8e1-101">Get-AzDefault</span></span>

## <span data-ttu-id="ca8e1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ca8e1-102">SYNOPSIS</span></span>
<span data-ttu-id="ca8e1-103">Hämta de standardvärden som användaren angett i den aktuella kontexten.</span><span class="sxs-lookup"><span data-stu-id="ca8e1-103">Get the defaults set by the user in the current context.</span></span>

## <span data-ttu-id="ca8e1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ca8e1-104">SYNTAX</span></span>

```
Get-AzDefault [-ResourceGroup] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca8e1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ca8e1-105">DESCRIPTION</span></span>
<span data-ttu-id="ca8e1-106">Get-AzDefault cmdlet får resurs gruppen att användaren har angett som standard i den aktuella kontexten.</span><span class="sxs-lookup"><span data-stu-id="ca8e1-106">The Get-AzDefault cmdlet gets the Resource Group that the user has set as default in the current context.</span></span>

## <span data-ttu-id="ca8e1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ca8e1-107">EXAMPLES</span></span>

### <span data-ttu-id="ca8e1-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ca8e1-108">Example 1</span></span>
```
PS C:\> Get-AzDefault

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="ca8e1-109">Det här kommandot returnerar de aktuella standardinställningarna om det finns standardinställningar eller om inget standardvärde anges.</span><span class="sxs-lookup"><span data-stu-id="ca8e1-109">This command returns the current defaults if there are defaults set, or returns nothing if no default is set.</span></span>

### <span data-ttu-id="ca8e1-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="ca8e1-110">Example 2</span></span>
```
PS C:\> Get-AzDefault -ResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="ca8e1-111">Det här kommandot returnerar den aktuella standard resurs gruppen om det finns en standard uppsättning eller om inget standardvärde har angetts.</span><span class="sxs-lookup"><span data-stu-id="ca8e1-111">This command returns the current default Resource Group if there is a default set, or returns nothing if no default is set.</span></span>

## <span data-ttu-id="ca8e1-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ca8e1-112">PARAMETERS</span></span>

### <span data-ttu-id="ca8e1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca8e1-113">-DefaultProfile</span></span>
<span data-ttu-id="ca8e1-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ca8e1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca8e1-115">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ca8e1-115">-ResourceGroup</span></span>
<span data-ttu-id="ca8e1-116">Visa standard resurs grupp</span><span class="sxs-lookup"><span data-stu-id="ca8e1-116">Display Default Resource Group</span></span>

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

### <span data-ttu-id="ca8e1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca8e1-117">CommonParameters</span></span>
<span data-ttu-id="ca8e1-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca8e1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca8e1-119">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca8e1-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca8e1-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ca8e1-120">INPUTS</span></span>

### <span data-ttu-id="ca8e1-121">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ca8e1-121">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ca8e1-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ca8e1-122">OUTPUTS</span></span>

### <span data-ttu-id="ca8e1-123">Microsoft. Azure. commands. Profile. Models. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ca8e1-123">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span></span>

## <span data-ttu-id="ca8e1-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ca8e1-124">NOTES</span></span>

## <span data-ttu-id="ca8e1-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ca8e1-125">RELATED LINKS</span></span>
