---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityContact.md
ms.openlocfilehash: b4cbecd2e29a0b70c7e62194df2364b22b33b462
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269961"
---
# <span data-ttu-id="12483-101">Remove-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="12483-101">Remove-AzSecurityContact</span></span>

## <span data-ttu-id="12483-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="12483-102">SYNOPSIS</span></span>
<span data-ttu-id="12483-103">Tar bort en säkerhets kontakt.</span><span class="sxs-lookup"><span data-stu-id="12483-103">Deletes a security contact.</span></span>

## <span data-ttu-id="12483-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="12483-104">SYNTAX</span></span>

### <span data-ttu-id="12483-105">SubscriptionLevelResource (standard)</span><span class="sxs-lookup"><span data-stu-id="12483-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityContact -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12483-106">ID</span><span class="sxs-lookup"><span data-stu-id="12483-106">ResourceId</span></span>
```
Remove-AzSecurityContact -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12483-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="12483-107">InputObject</span></span>
```
Remove-AzSecurityContact -InputObject <PSSecurityContact> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12483-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="12483-108">DESCRIPTION</span></span>
<span data-ttu-id="12483-109">Tar bort en säkerhets kontakt.</span><span class="sxs-lookup"><span data-stu-id="12483-109">Deletes a security contact.</span></span>

## <span data-ttu-id="12483-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="12483-110">EXAMPLES</span></span>

### <span data-ttu-id="12483-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="12483-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityContact -Name "default1"
```

<span data-ttu-id="12483-112">Tar bort säkerhets kontakten "default1"</span><span class="sxs-lookup"><span data-stu-id="12483-112">Deletes the "default1" security contact</span></span>

## <span data-ttu-id="12483-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="12483-113">PARAMETERS</span></span>

### <span data-ttu-id="12483-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12483-114">-DefaultProfile</span></span>
<span data-ttu-id="12483-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="12483-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12483-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="12483-116">-InputObject</span></span>
<span data-ttu-id="12483-117">Indatavärdet.</span><span class="sxs-lookup"><span data-stu-id="12483-117">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12483-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="12483-118">-Name</span></span>
<span data-ttu-id="12483-119">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="12483-119">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12483-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="12483-120">-PassThru</span></span>
<span data-ttu-id="12483-121">Returnera om åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="12483-121">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="12483-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12483-122">-ResourceId</span></span>
<span data-ttu-id="12483-123">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="12483-123">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12483-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="12483-124">-Confirm</span></span>
<span data-ttu-id="12483-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="12483-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12483-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12483-126">-WhatIf</span></span>
<span data-ttu-id="12483-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="12483-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="12483-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="12483-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12483-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12483-129">CommonParameters</span></span>
<span data-ttu-id="12483-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12483-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12483-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="12483-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12483-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="12483-132">INPUTS</span></span>

### <span data-ttu-id="12483-133">System. String</span><span class="sxs-lookup"><span data-stu-id="12483-133">System.String</span></span>

### <span data-ttu-id="12483-134">Microsoft. Azure. commands. Security. Models. SecurityContacts. PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="12483-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="12483-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="12483-135">OUTPUTS</span></span>

### <span data-ttu-id="12483-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="12483-136">System.Boolean</span></span>

## <span data-ttu-id="12483-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="12483-137">NOTES</span></span>

## <span data-ttu-id="12483-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="12483-138">RELATED LINKS</span></span>
