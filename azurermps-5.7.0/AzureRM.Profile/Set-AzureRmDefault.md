---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/set-azurermdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmDefault.md
ms.openlocfilehash: 01b8283277c1d9592adbd8edfe6b883a4451ded9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756479"
---
# <span data-ttu-id="92cdc-101">Set-AzureRmDefault</span><span class="sxs-lookup"><span data-stu-id="92cdc-101">Set-AzureRmDefault</span></span>

## <span data-ttu-id="92cdc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="92cdc-102">SYNOPSIS</span></span>
<span data-ttu-id="92cdc-103">Anger en standard i den aktuella kontexten</span><span class="sxs-lookup"><span data-stu-id="92cdc-103">Sets a default in the current context</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92cdc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="92cdc-104">SYNTAX</span></span>

```
Set-AzureRmDefault [-ResourceGroupName <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92cdc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="92cdc-105">DESCRIPTION</span></span>
<span data-ttu-id="92cdc-106">Set-AzureRmDefault cmdlet lägger till eller ändrar standardvärden i den aktuella kontexten.</span><span class="sxs-lookup"><span data-stu-id="92cdc-106">The Set-AzureRmDefault cmdlet adds or changes the defaults in the current context.</span></span>

## <span data-ttu-id="92cdc-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="92cdc-107">EXAMPLES</span></span>

### <span data-ttu-id="92cdc-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="92cdc-108">Example 1</span></span>
```
PS C:\> Set-AzureRmDefault -ResourceGroupName myResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="92cdc-109">Det här kommandot anger standard resurs gruppen till den resurs grupp som användaren angett.</span><span class="sxs-lookup"><span data-stu-id="92cdc-109">This command sets the default resource group to the resource group specified by the user.</span></span>

## <span data-ttu-id="92cdc-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="92cdc-110">PARAMETERS</span></span>

### <span data-ttu-id="92cdc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92cdc-111">-DefaultProfile</span></span>
<span data-ttu-id="92cdc-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="92cdc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92cdc-113">-Force</span><span class="sxs-lookup"><span data-stu-id="92cdc-113">-Force</span></span>
<span data-ttu-id="92cdc-114">Skapa en ny resurs grupp om det angivna standardvärdet inte finns</span><span class="sxs-lookup"><span data-stu-id="92cdc-114">Create a new resource group if specified default does not exist</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92cdc-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92cdc-115">-ResourceGroupName</span></span>
<span data-ttu-id="92cdc-116">Namnet på den resurs grupp som ska anges som standard</span><span class="sxs-lookup"><span data-stu-id="92cdc-116">Name of the resource group being set as default</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92cdc-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="92cdc-117">-Confirm</span></span>
<span data-ttu-id="92cdc-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="92cdc-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92cdc-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92cdc-119">-WhatIf</span></span>
<span data-ttu-id="92cdc-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="92cdc-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92cdc-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="92cdc-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92cdc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92cdc-122">CommonParameters</span></span>
<span data-ttu-id="92cdc-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92cdc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92cdc-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92cdc-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92cdc-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="92cdc-125">INPUTS</span></span>

### <span data-ttu-id="92cdc-126">System. String</span><span class="sxs-lookup"><span data-stu-id="92cdc-126">System.String</span></span>

## <span data-ttu-id="92cdc-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="92cdc-127">OUTPUTS</span></span>

### <span data-ttu-id="92cdc-128">Microsoft. Azure. Management. Internal. Resources. Models. ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="92cdc-128">Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroup</span></span>

## <span data-ttu-id="92cdc-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="92cdc-129">NOTES</span></span>

## <span data-ttu-id="92cdc-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="92cdc-130">RELATED LINKS</span></span>

