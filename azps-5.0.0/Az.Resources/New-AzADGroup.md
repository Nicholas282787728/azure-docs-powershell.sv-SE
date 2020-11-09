---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
ms.openlocfilehash: 98d87c060c51d19db45e907f88d39f27350248c9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322847"
---
# <span data-ttu-id="85673-101">New-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="85673-101">New-AzADGroup</span></span>

## <span data-ttu-id="85673-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="85673-102">SYNOPSIS</span></span>
<span data-ttu-id="85673-103">Skapar en ny Active Directory-grupp.</span><span class="sxs-lookup"><span data-stu-id="85673-103">Creates a new active directory group.</span></span>

## <span data-ttu-id="85673-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="85673-104">SYNTAX</span></span>

```
New-AzADGroup -DisplayName <String> -MailNickname <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85673-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="85673-105">DESCRIPTION</span></span>
<span data-ttu-id="85673-106">Skapar en ny Active Directory-grupp. Här är de behörigheter som behövs:</span><span class="sxs-lookup"><span data-stu-id="85673-106">Creates a new active directory group.Below are the permissions needed:</span></span>

- <span data-ttu-id="85673-107">Azure Active Directory-diagram</span><span class="sxs-lookup"><span data-stu-id="85673-107">Azure Active Directory Graph</span></span>
  - <span data-ttu-id="85673-108">Directory. ReadWrite. all</span><span class="sxs-lookup"><span data-stu-id="85673-108">Directory.ReadWrite.All</span></span>
- <span data-ttu-id="85673-109">Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="85673-109">Microsoft Graph</span></span>
  - <span data-ttu-id="85673-110">Directory. ReadWrite. all</span><span class="sxs-lookup"><span data-stu-id="85673-110">Directory.ReadWrite.All</span></span>
  - <span data-ttu-id="85673-111">PrivilegedAccess. ReadWrite. AzureADGroup</span><span class="sxs-lookup"><span data-stu-id="85673-111">PrivilegedAccess.ReadWrite.AzureADGroup</span></span>

## <span data-ttu-id="85673-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="85673-112">EXAMPLES</span></span>

### <span data-ttu-id="85673-113">Exempel 1: skapa en ny AD-grupp</span><span class="sxs-lookup"><span data-stu-id="85673-113">Example 1: Create a new AD group</span></span>

```powershell
PS C:\> New-AzADGroup -DisplayName "MyGroupDisplayName" -MailNickname "MyGroupNick"
```

<span data-ttu-id="85673-114">Skapar en ny AD-grupp med namnet "MyGroupDisplayName" och e-postsmek namnet "MyGroupNick".</span><span class="sxs-lookup"><span data-stu-id="85673-114">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "MyGroupNick".</span></span>

## <span data-ttu-id="85673-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="85673-115">PARAMETERS</span></span>

### <span data-ttu-id="85673-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85673-116">-DefaultProfile</span></span>
<span data-ttu-id="85673-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="85673-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85673-118">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="85673-118">-Description</span></span>
<span data-ttu-id="85673-119">Beskrivning för gruppen.</span><span class="sxs-lookup"><span data-stu-id="85673-119">The description for the group.</span></span>

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

### <span data-ttu-id="85673-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="85673-120">-DisplayName</span></span>
<span data-ttu-id="85673-121">Gruppens visnings namn.</span><span class="sxs-lookup"><span data-stu-id="85673-121">The display name for the group.</span></span>

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

### <span data-ttu-id="85673-122">-Smek namn</span><span class="sxs-lookup"><span data-stu-id="85673-122">-MailNickname</span></span>
<span data-ttu-id="85673-123">E-postsmek för gruppen.</span><span class="sxs-lookup"><span data-stu-id="85673-123">The mail nickname for the group.</span></span> <span data-ttu-id="85673-124">Får inte innehålla tecknet @.</span><span class="sxs-lookup"><span data-stu-id="85673-124">Cannot contain the @ sign.</span></span>

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

### <span data-ttu-id="85673-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="85673-125">-Confirm</span></span>
<span data-ttu-id="85673-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="85673-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85673-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85673-127">-WhatIf</span></span>
<span data-ttu-id="85673-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="85673-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85673-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="85673-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85673-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85673-130">CommonParameters</span></span>
<span data-ttu-id="85673-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85673-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85673-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="85673-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85673-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="85673-133">INPUTS</span></span>

### <span data-ttu-id="85673-134">System. String</span><span class="sxs-lookup"><span data-stu-id="85673-134">System.String</span></span>

## <span data-ttu-id="85673-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="85673-135">OUTPUTS</span></span>

### <span data-ttu-id="85673-136">Microsoft. Azure. commands. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="85673-136">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="85673-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="85673-137">NOTES</span></span>

## <span data-ttu-id="85673-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="85673-138">RELATED LINKS</span></span>
