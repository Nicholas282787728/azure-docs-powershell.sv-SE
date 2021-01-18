---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSqlInformationProtectionPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSqlInformationProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSqlInformationProtectionPolicy.md
ms.openlocfilehash: 3b433860cda56f827bb58bc135240da41b89ef93
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525607"
---
# <span data-ttu-id="11dad-101">Set-AzSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="11dad-101">Set-AzSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="11dad-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="11dad-102">SYNOPSIS</span></span>
<span data-ttu-id="11dad-103">Anger den effektiva policyn för informations skydd i klient organisationen.</span><span class="sxs-lookup"><span data-stu-id="11dad-103">Sets the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="11dad-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="11dad-104">SYNTAX</span></span>

### <span data-ttu-id="11dad-105">Policy för informations skydd i SQL (standard)</span><span class="sxs-lookup"><span data-stu-id="11dad-105">SQL Information Protection Policy (Default)</span></span>
```
Set-AzSqlInformationProtectionPolicy -Policy <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11dad-106">Sökväg till princip fil för SQL information Protection</span><span class="sxs-lookup"><span data-stu-id="11dad-106">SQL Information Protection Policy File Path</span></span>
```
Set-AzSqlInformationProtectionPolicy -FilePath <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11dad-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="11dad-107">DESCRIPTION</span></span>
<span data-ttu-id="11dad-108">Anger den effektiva policyn för informations skydd i klient organisationen.</span><span class="sxs-lookup"><span data-stu-id="11dad-108">Sets the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="11dad-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="11dad-109">EXAMPLES</span></span>

### <span data-ttu-id="11dad-110">Exempel</span><span class="sxs-lookup"><span data-stu-id="11dad-110">Example</span></span>
```powershell
PS C:\> Set-AzSqlInformationProtectionPolicy -FilePath "C:\Users\myUser\Desktop\policy.json"
```

## <span data-ttu-id="11dad-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="11dad-111">PARAMETERS</span></span>

### <span data-ttu-id="11dad-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="11dad-112">-AsJob</span></span>
<span data-ttu-id="11dad-113">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="11dad-113">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11dad-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11dad-114">-DefaultProfile</span></span>
<span data-ttu-id="11dad-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="11dad-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11dad-116">-Sökväg</span><span class="sxs-lookup"><span data-stu-id="11dad-116">-FilePath</span></span>
<span data-ttu-id="11dad-117">Anger en sökväg till en. JSON-fil som innehåller princip definitionen för SQL information Protection.</span><span class="sxs-lookup"><span data-stu-id="11dad-117">Specifies a path of a .json file containing SQL Information Protection Policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: SQL Information Protection Policy File Path
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11dad-118">-Princip</span><span class="sxs-lookup"><span data-stu-id="11dad-118">-Policy</span></span>
<span data-ttu-id="11dad-119">Anger en SQL policy-definition för informations skydd.</span><span class="sxs-lookup"><span data-stu-id="11dad-119">Specifies a SQL information protection policy definition.</span></span> <span data-ttu-id="11dad-120">Du kan ange en sökväg till en. JSON-fil eller en JSON format-sträng som definierar principen.</span><span class="sxs-lookup"><span data-stu-id="11dad-120">You can specify a path of a .json file or a JSON format string that defines the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: SQL Information Protection Policy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11dad-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="11dad-121">-Confirm</span></span>
<span data-ttu-id="11dad-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="11dad-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11dad-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11dad-123">-WhatIf</span></span>
<span data-ttu-id="11dad-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="11dad-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="11dad-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="11dad-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11dad-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11dad-126">CommonParameters</span></span>
<span data-ttu-id="11dad-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11dad-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11dad-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="11dad-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11dad-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="11dad-129">INPUTS</span></span>

### <span data-ttu-id="11dad-130">System. String</span><span class="sxs-lookup"><span data-stu-id="11dad-130">System.String</span></span>

## <span data-ttu-id="11dad-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="11dad-131">OUTPUTS</span></span>

### <span data-ttu-id="11dad-132">Microsoft. Azure. commands. SecurityCenter. Models. SqlInformationProtectionPolicy. PSSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="11dad-132">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="11dad-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="11dad-133">NOTES</span></span>

## <span data-ttu-id="11dad-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="11dad-134">RELATED LINKS</span></span>
