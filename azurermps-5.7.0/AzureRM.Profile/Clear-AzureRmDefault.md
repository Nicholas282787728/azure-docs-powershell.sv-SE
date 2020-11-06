---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/clear-azurermdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Clear-AzureRmDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Clear-AzureRmDefault.md
ms.openlocfilehash: 4f3a463f8ae03dcbefaf9588ca196f01955070ef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573387"
---
# <span data-ttu-id="4d562-101">Clear-AzureRmDefault</span><span class="sxs-lookup"><span data-stu-id="4d562-101">Clear-AzureRmDefault</span></span>

## <span data-ttu-id="4d562-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4d562-102">SYNOPSIS</span></span>
<span data-ttu-id="4d562-103">Rensar standardinställningarna som anges av användaren i den aktuella kontexten.</span><span class="sxs-lookup"><span data-stu-id="4d562-103">Clears the defaults set by the user in the current context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d562-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4d562-104">SYNTAX</span></span>

```
Clear-AzureRmDefault [-ResourceGroup] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d562-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4d562-105">DESCRIPTION</span></span>
<span data-ttu-id="4d562-106">Clear-AzureRmDefault cmdlet tar bort standardvärdena som anges av användaren, beroende på parametrarna som anges av användaren.</span><span class="sxs-lookup"><span data-stu-id="4d562-106">The Clear-AzureRmDefault cmdlet removes the defaults set by the user depending on the switch parameters specified by the user.</span></span>

## <span data-ttu-id="4d562-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4d562-107">EXAMPLES</span></span>

### <span data-ttu-id="4d562-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4d562-108">Example 1</span></span>
```
PS C:\> Clear-AzureRmDefault
```

<span data-ttu-id="4d562-109">Det här kommandot tar bort alla standardinställningar som anges av användaren i den aktuella kontexten.</span><span class="sxs-lookup"><span data-stu-id="4d562-109">This command removes all the defaults set by the user in the current context.</span></span>

### <span data-ttu-id="4d562-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4d562-110">Example 1</span></span>
```
PS C:\> Clear-AzureRmDefault -ResourceGroup
```

<span data-ttu-id="4d562-111">Det här kommandot tar bort standard resurs gruppen som anges av användaren i den aktuella kontexten.</span><span class="sxs-lookup"><span data-stu-id="4d562-111">This command removes the default resource group set by the user in the current context.</span></span>

## <span data-ttu-id="4d562-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4d562-112">PARAMETERS</span></span>

### <span data-ttu-id="4d562-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d562-113">-DefaultProfile</span></span>
<span data-ttu-id="4d562-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4d562-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d562-115">-Force</span><span class="sxs-lookup"><span data-stu-id="4d562-115">-Force</span></span>
<span data-ttu-id="4d562-116">Ta bort alla standarder om inget standardvärde anges</span><span class="sxs-lookup"><span data-stu-id="4d562-116">Remove all defaults if no default is specified</span></span>

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

### <span data-ttu-id="4d562-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4d562-117">-PassThru</span></span>
<span data-ttu-id="4d562-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="4d562-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="4d562-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4d562-119">-ResourceGroup</span></span>
<span data-ttu-id="4d562-120">Rensa standard resurs grupp</span><span class="sxs-lookup"><span data-stu-id="4d562-120">Clear Default Resource Group</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d562-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4d562-121">-Confirm</span></span>
<span data-ttu-id="4d562-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4d562-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d562-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d562-123">-WhatIf</span></span>
<span data-ttu-id="4d562-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4d562-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d562-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4d562-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d562-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d562-126">CommonParameters</span></span>
<span data-ttu-id="4d562-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d562-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d562-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d562-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d562-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4d562-129">INPUTS</span></span>

### <span data-ttu-id="4d562-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4d562-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4d562-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4d562-131">OUTPUTS</span></span>

### <span data-ttu-id="4d562-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="4d562-132">System.Object</span></span>

## <span data-ttu-id="4d562-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4d562-133">NOTES</span></span>

## <span data-ttu-id="4d562-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4d562-134">RELATED LINKS</span></span>

