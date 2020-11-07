---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: D28EB28D-DBC6-48D5-AB0A-C56F56CD0104
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/set-azurermmediaservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Set-AzureRmMediaServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Set-AzureRmMediaServiceKey.md
ms.openlocfilehash: 10de62fd77fa62f83373637e844edd436dd0681f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584956"
---
# <span data-ttu-id="d3728-101">Set-AzureRmMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="d3728-101">Set-AzureRmMediaServiceKey</span></span>

## <span data-ttu-id="d3728-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d3728-102">SYNOPSIS</span></span>
<span data-ttu-id="d3728-103">Återskapar en nyckeln som används för att komma åt den REST-slutpunkt som är associerad med medie tjänsten.</span><span class="sxs-lookup"><span data-stu-id="d3728-103">Regenerates a key used for accessing the REST endpoint associated with the media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3728-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d3728-104">SYNTAX</span></span>

```
Set-AzureRmMediaServiceKey [-ResourceGroupName] <String> [-AccountName] <String> [-KeyType] <KeyType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3728-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d3728-105">DESCRIPTION</span></span>
<span data-ttu-id="d3728-106">Cmdleten **set-AzureRmMediaServiceKey** återskapar en nyckeln som används för att öppna den ompresentations tillstånds överföring (rest) som är associerad med medie tjänsten.</span><span class="sxs-lookup"><span data-stu-id="d3728-106">The **Set-AzureRmMediaServiceKey** cmdlet regenerates a key used for accessing the Representational State Transfer (REST) endpoint associated with the media service.</span></span>

## <span data-ttu-id="d3728-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d3728-107">EXAMPLES</span></span>

### <span data-ttu-id="d3728-108">Exempel 1: återskapa den primära nyckeln som används för åtkomst till medie tjänsten</span><span class="sxs-lookup"><span data-stu-id="d3728-108">Example 1: Regenerate the primary key used for accessing the Media Service</span></span>
```
PS C:\>Set-AzureRmMediaServiceKey -ResourceGroupName "ResourceGroup004" -AccountName "MediaService001" -KeyType Primary
```

<span data-ttu-id="d3728-109">Det här kommandot återskapar primär nyckeln för medie tjänsten som heter MediaService001 som tillhör resurs gruppen med namnet ResourceGroup004.</span><span class="sxs-lookup"><span data-stu-id="d3728-109">This command regenerates the primary key for the media service named MediaService001 that belongs to the resource group named ResourceGroup004.</span></span>

### <span data-ttu-id="d3728-110">Exempel 2: återskapa den sekundära nyckeln som används för åtkomst till medie tjänsten</span><span class="sxs-lookup"><span data-stu-id="d3728-110">Example 2: Regenerates the secondary key used for accessing the Media Service</span></span>
```
PS C:\>Set-AzureRmMediaServiceKey -ResourceGroupName "Resourcegroup123" -AccountName "MediaService002" -KeyType Secondary
```

<span data-ttu-id="d3728-111">Det här kommandot återskapar den sekundära nyckeln för medie tjänsten som heter MediaService002 som tillhör resurs gruppen med namnet Resourcegroup123.</span><span class="sxs-lookup"><span data-stu-id="d3728-111">This command regenerates the secondary key for the media service named MediaService002 that belongs to the resource group named Resourcegroup123.</span></span>

## <span data-ttu-id="d3728-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d3728-112">PARAMETERS</span></span>

### <span data-ttu-id="d3728-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d3728-113">-AccountName</span></span>
<span data-ttu-id="d3728-114">Anger namnet på den medie tjänst som denna cmdlet ska återskapa.</span><span class="sxs-lookup"><span data-stu-id="d3728-114">Specifies the name of the media service that this cmdlet regenerates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3728-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3728-115">-DefaultProfile</span></span>
<span data-ttu-id="d3728-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d3728-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3728-117">-Värdetyp</span><span class="sxs-lookup"><span data-stu-id="d3728-117">-KeyType</span></span>
<span data-ttu-id="d3728-118">Anger medie tjänstens medietyp.</span><span class="sxs-lookup"><span data-stu-id="d3728-118">Specifies the key type of the media service.</span></span>
<span data-ttu-id="d3728-119">De acceptabla värdena för den här parametern är: primär eller sekundär.</span><span class="sxs-lookup"><span data-stu-id="d3728-119">The acceptable values for this parameter are: Primary or Secondary.</span></span>

```yaml
Type: Microsoft.Azure.Management.Media.Models.KeyType
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3728-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3728-120">-ResourceGroupName</span></span>
<span data-ttu-id="d3728-121">Anger namnet på den resurs grupp som innehåller medie tjänsten.</span><span class="sxs-lookup"><span data-stu-id="d3728-121">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="d3728-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d3728-122">-Confirm</span></span>
<span data-ttu-id="d3728-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d3728-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3728-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3728-124">-WhatIf</span></span>
<span data-ttu-id="d3728-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d3728-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3728-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d3728-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3728-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3728-127">CommonParameters</span></span>
<span data-ttu-id="d3728-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3728-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3728-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3728-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3728-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d3728-130">INPUTS</span></span>

### <span data-ttu-id="d3728-131">System. String</span><span class="sxs-lookup"><span data-stu-id="d3728-131">System.String</span></span>

## <span data-ttu-id="d3728-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d3728-132">OUTPUTS</span></span>

### <span data-ttu-id="d3728-133">Microsoft. Azure. commands. Media. Models. PSServiceKey</span><span class="sxs-lookup"><span data-stu-id="d3728-133">Microsoft.Azure.Commands.Media.Models.PSServiceKey</span></span>

## <span data-ttu-id="d3728-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d3728-134">NOTES</span></span>

## <span data-ttu-id="d3728-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d3728-135">RELATED LINKS</span></span>

[<span data-ttu-id="d3728-136">Get-AzureRmMediaServiceKeys</span><span class="sxs-lookup"><span data-stu-id="d3728-136">Get-AzureRmMediaServiceKeys</span></span>](./Get-AzureRmMediaServiceKeys.md)

