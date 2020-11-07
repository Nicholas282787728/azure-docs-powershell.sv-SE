---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADGroup.md
ms.openlocfilehash: b5bc2f2eb99a8256dcaa6bc4f026d922f0f563ea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923965"
---
# <span data-ttu-id="e84d7-101">New-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="e84d7-101">New-AzADGroup</span></span>

## <span data-ttu-id="e84d7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e84d7-102">SYNOPSIS</span></span>
<span data-ttu-id="e84d7-103">Skapar en ny Active Directory-grupp.</span><span class="sxs-lookup"><span data-stu-id="e84d7-103">Creates a new active directory group.</span></span>

## <span data-ttu-id="e84d7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e84d7-104">SYNTAX</span></span>

```
New-AzADGroup -DisplayName <String> -MailNickname <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e84d7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e84d7-105">DESCRIPTION</span></span>
<span data-ttu-id="e84d7-106">Skapar en ny Active Directory-grupp.</span><span class="sxs-lookup"><span data-stu-id="e84d7-106">Creates a new active directory group.</span></span>

## <span data-ttu-id="e84d7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e84d7-107">EXAMPLES</span></span>

### <span data-ttu-id="e84d7-108">Exempel 1 – Skapa en ny AD-grupp</span><span class="sxs-lookup"><span data-stu-id="e84d7-108">Example 1 - Create a new AD group</span></span>

```
PS C:\> New-AzADGroup -DisplayName "MyGroupDisplayName" -MailNickname "myemail@domain.com"
```

<span data-ttu-id="e84d7-109">Skapar en ny AD-grupp med namnet "MyGroupDisplayName" och "e-postnamn" myemail@domain.com ".</span><span class="sxs-lookup"><span data-stu-id="e84d7-109">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "myemail@domain.com".</span></span>

## <span data-ttu-id="e84d7-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e84d7-110">PARAMETERS</span></span>

### <span data-ttu-id="e84d7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e84d7-111">-DefaultProfile</span></span>
<span data-ttu-id="e84d7-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e84d7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e84d7-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e84d7-113">-DisplayName</span></span>
<span data-ttu-id="e84d7-114">Gruppens visnings namn.</span><span class="sxs-lookup"><span data-stu-id="e84d7-114">The display name for the group.</span></span>

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

### <span data-ttu-id="e84d7-115">-Smek namn</span><span class="sxs-lookup"><span data-stu-id="e84d7-115">-MailNickname</span></span>
<span data-ttu-id="e84d7-116">E-postsmek för gruppen.</span><span class="sxs-lookup"><span data-stu-id="e84d7-116">The mail nickname for the group.</span></span>

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

### <span data-ttu-id="e84d7-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e84d7-117">-Confirm</span></span>
<span data-ttu-id="e84d7-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e84d7-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e84d7-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e84d7-119">-WhatIf</span></span>
<span data-ttu-id="e84d7-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e84d7-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e84d7-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e84d7-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e84d7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e84d7-122">CommonParameters</span></span>
<span data-ttu-id="e84d7-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e84d7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e84d7-124">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e84d7-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e84d7-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e84d7-125">INPUTS</span></span>

### <span data-ttu-id="e84d7-126">System. String</span><span class="sxs-lookup"><span data-stu-id="e84d7-126">System.String</span></span>

## <span data-ttu-id="e84d7-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e84d7-127">OUTPUTS</span></span>

### <span data-ttu-id="e84d7-128">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="e84d7-128">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="e84d7-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e84d7-129">NOTES</span></span>

## <span data-ttu-id="e84d7-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e84d7-130">RELATED LINKS</span></span>
