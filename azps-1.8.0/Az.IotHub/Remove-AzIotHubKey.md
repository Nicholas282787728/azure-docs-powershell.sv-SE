---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
ms.openlocfilehash: c275ac087c24c58de73e72ac5dcf46839d710621
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916418"
---
# <span data-ttu-id="c69f2-101">Remove-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="c69f2-101">Remove-AzIotHubKey</span></span>

## <span data-ttu-id="c69f2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c69f2-102">SYNOPSIS</span></span>
<span data-ttu-id="c69f2-103">Tar bort en IotHub-tangenten.</span><span class="sxs-lookup"><span data-stu-id="c69f2-103">Removes an IotHub Key.</span></span>

## <span data-ttu-id="c69f2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c69f2-104">SYNTAX</span></span>

```
Remove-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c69f2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c69f2-105">DESCRIPTION</span></span>
<span data-ttu-id="c69f2-106">Tar bort en IotHub-tangenten.</span><span class="sxs-lookup"><span data-stu-id="c69f2-106">Removes an IotHub Key.</span></span>
<span data-ttu-id="c69f2-107">Om det finns flera tangenter med samma namn tas den första i listan bort.</span><span class="sxs-lookup"><span data-stu-id="c69f2-107">If there are multiple keys with the same name the first one in the list is removed.</span></span>

## <span data-ttu-id="c69f2-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c69f2-108">EXAMPLES</span></span>

### <span data-ttu-id="c69f2-109">Exempel 1 ta bort en IotHub</span><span class="sxs-lookup"><span data-stu-id="c69f2-109">Example 1 Delete an IotHub</span></span>
```
PS C:\> Remove-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner1"
```

<span data-ttu-id="c69f2-110">Tar bort den iothubowner1 från IotHub som heter "myiothub"</span><span class="sxs-lookup"><span data-stu-id="c69f2-110">Removes the key named iothubowner1 from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="c69f2-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c69f2-111">PARAMETERS</span></span>

### <span data-ttu-id="c69f2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c69f2-112">-DefaultProfile</span></span>
<span data-ttu-id="c69f2-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c69f2-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c69f2-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="c69f2-114">-KeyName</span></span>
<span data-ttu-id="c69f2-115">Namnet på tangenten</span><span class="sxs-lookup"><span data-stu-id="c69f2-115">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c69f2-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="c69f2-116">-Name</span></span>
<span data-ttu-id="c69f2-117">Namn på IotHub</span><span class="sxs-lookup"><span data-stu-id="c69f2-117">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c69f2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c69f2-118">-ResourceGroupName</span></span>
<span data-ttu-id="c69f2-119">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="c69f2-119">Resource Group Name</span></span>

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

### <span data-ttu-id="c69f2-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c69f2-120">-Confirm</span></span>
<span data-ttu-id="c69f2-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c69f2-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c69f2-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c69f2-122">-WhatIf</span></span>
<span data-ttu-id="c69f2-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c69f2-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c69f2-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c69f2-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c69f2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c69f2-125">CommonParameters</span></span>
<span data-ttu-id="c69f2-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c69f2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c69f2-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c69f2-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c69f2-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c69f2-128">INPUTS</span></span>

### <span data-ttu-id="c69f2-129">System. String</span><span class="sxs-lookup"><span data-stu-id="c69f2-129">System.String</span></span>

## <span data-ttu-id="c69f2-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c69f2-130">OUTPUTS</span></span>

### <span data-ttu-id="c69f2-131">Microsoft. Azure. commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c69f2-131">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="c69f2-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c69f2-132">NOTES</span></span>

## <span data-ttu-id="c69f2-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c69f2-133">RELATED LINKS</span></span>
