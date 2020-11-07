---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Remove-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Remove-AzIotHub.md
ms.openlocfilehash: 0e83ec5266bc807f64bd231a3a423ad8cc7db190
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924506"
---
# <span data-ttu-id="2ee46-101">Remove-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="2ee46-101">Remove-AzIotHub</span></span>

## <span data-ttu-id="2ee46-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2ee46-102">SYNOPSIS</span></span>
<span data-ttu-id="2ee46-103">Tar bort en IotHub.</span><span class="sxs-lookup"><span data-stu-id="2ee46-103">Deletes an IotHub.</span></span>

## <span data-ttu-id="2ee46-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2ee46-104">SYNTAX</span></span>

```
Remove-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ee46-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2ee46-105">DESCRIPTION</span></span>
<span data-ttu-id="2ee46-106">Tar bort en IotHub.</span><span class="sxs-lookup"><span data-stu-id="2ee46-106">Deletes an IotHub.</span></span>

## <span data-ttu-id="2ee46-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2ee46-107">EXAMPLES</span></span>

### <span data-ttu-id="2ee46-108">Exempel 1 ta bort en IotHub</span><span class="sxs-lookup"><span data-stu-id="2ee46-108">Example 1 Remove an IotHub</span></span>
```
PS C:\> Remove-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="2ee46-109">Tar bort en IotHub med namnet "myiothub"</span><span class="sxs-lookup"><span data-stu-id="2ee46-109">Removes an IotHub named "myiothub"</span></span>

## <span data-ttu-id="2ee46-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2ee46-110">PARAMETERS</span></span>

### <span data-ttu-id="2ee46-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ee46-111">-DefaultProfile</span></span>
<span data-ttu-id="2ee46-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="2ee46-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2ee46-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="2ee46-113">-Name</span></span>
<span data-ttu-id="2ee46-114">Namn på IotHub</span><span class="sxs-lookup"><span data-stu-id="2ee46-114">Name of the IotHub</span></span>

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

### <span data-ttu-id="2ee46-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ee46-115">-ResourceGroupName</span></span>
<span data-ttu-id="2ee46-116">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="2ee46-116">Resource Group Name</span></span>

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

### <span data-ttu-id="2ee46-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2ee46-117">-Confirm</span></span>
<span data-ttu-id="2ee46-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2ee46-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ee46-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ee46-119">-WhatIf</span></span>
<span data-ttu-id="2ee46-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2ee46-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ee46-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2ee46-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ee46-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ee46-122">CommonParameters</span></span>
<span data-ttu-id="2ee46-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ee46-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ee46-124">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ee46-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ee46-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2ee46-125">INPUTS</span></span>

### <span data-ttu-id="2ee46-126">System. String</span><span class="sxs-lookup"><span data-stu-id="2ee46-126">System.String</span></span>

## <span data-ttu-id="2ee46-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2ee46-127">OUTPUTS</span></span>

### <span data-ttu-id="2ee46-128">System. Void</span><span class="sxs-lookup"><span data-stu-id="2ee46-128">System.Void</span></span>

## <span data-ttu-id="2ee46-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2ee46-129">NOTES</span></span>

## <span data-ttu-id="2ee46-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2ee46-130">RELATED LINKS</span></span>
