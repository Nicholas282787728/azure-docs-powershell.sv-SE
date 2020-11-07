---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
ms.openlocfilehash: d1a5057b25c08d1c93512ad3f439a9b4b208552f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919309"
---
# <span data-ttu-id="0dfd7-101">New-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="0dfd7-101">New-AzADGroup</span></span>

## <span data-ttu-id="0dfd7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0dfd7-102">SYNOPSIS</span></span>
<span data-ttu-id="0dfd7-103">Skapar en ny Active Directory-grupp.</span><span class="sxs-lookup"><span data-stu-id="0dfd7-103">Creates a new active directory group.</span></span>

## <span data-ttu-id="0dfd7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0dfd7-104">SYNTAX</span></span>

```
New-AzADGroup -DisplayName <String> -MailNickname <String> [-Description <string>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0dfd7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0dfd7-105">DESCRIPTION</span></span>
<span data-ttu-id="0dfd7-106">Skapar en ny Active Directory-grupp.</span><span class="sxs-lookup"><span data-stu-id="0dfd7-106">Creates a new active directory group.</span></span>

## <span data-ttu-id="0dfd7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0dfd7-107">EXAMPLES</span></span>

### <span data-ttu-id="0dfd7-108">Exempel 1 – Skapa en ny AD-grupp</span><span class="sxs-lookup"><span data-stu-id="0dfd7-108">Example 1 - Create a new AD group</span></span>

```
PS C:\> New-AzADGroup -DisplayName "MyGroupDisplayName" -MailNickname "MyGroupNick"
```

<span data-ttu-id="0dfd7-109">Skapar en ny AD-grupp med namnet "MyGroupDisplayName" och e-postsmek namnet "MyGroupNick".</span><span class="sxs-lookup"><span data-stu-id="0dfd7-109">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "MyGroupNick".</span></span>

## <span data-ttu-id="0dfd7-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0dfd7-110">PARAMETERS</span></span>

### <span data-ttu-id="0dfd7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dfd7-111">-DefaultProfile</span></span>
<span data-ttu-id="0dfd7-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0dfd7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0dfd7-113">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="0dfd7-113">-Description</span></span>
<span data-ttu-id="0dfd7-114">Beskrivning för gruppen.</span><span class="sxs-lookup"><span data-stu-id="0dfd7-114">The description for the group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0dfd7-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="0dfd7-115">-DisplayName</span></span>
<span data-ttu-id="0dfd7-116">Gruppens visnings namn.</span><span class="sxs-lookup"><span data-stu-id="0dfd7-116">The display name for the group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0dfd7-117">-Smek namn</span><span class="sxs-lookup"><span data-stu-id="0dfd7-117">-MailNickname</span></span>
<span data-ttu-id="0dfd7-118">E-postsmek för gruppen.</span><span class="sxs-lookup"><span data-stu-id="0dfd7-118">The mail nickname for the group.</span></span> <span data-ttu-id="0dfd7-119">Får inte innehålla tecknet @.</span><span class="sxs-lookup"><span data-stu-id="0dfd7-119">Cannot contain the @ sign.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0dfd7-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0dfd7-120">-Confirm</span></span>
<span data-ttu-id="0dfd7-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0dfd7-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dfd7-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0dfd7-122">-WhatIf</span></span>
<span data-ttu-id="0dfd7-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0dfd7-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0dfd7-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0dfd7-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dfd7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dfd7-125">CommonParameters</span></span>
<span data-ttu-id="0dfd7-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0dfd7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dfd7-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0dfd7-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dfd7-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0dfd7-128">INPUTS</span></span>

### <span data-ttu-id="0dfd7-129">System. String</span><span class="sxs-lookup"><span data-stu-id="0dfd7-129">System.String</span></span>

## <span data-ttu-id="0dfd7-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0dfd7-130">OUTPUTS</span></span>

### <span data-ttu-id="0dfd7-131">Microsoft. Azure. commands. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="0dfd7-131">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="0dfd7-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0dfd7-132">NOTES</span></span>

## <span data-ttu-id="0dfd7-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0dfd7-133">RELATED LINKS</span></span>
