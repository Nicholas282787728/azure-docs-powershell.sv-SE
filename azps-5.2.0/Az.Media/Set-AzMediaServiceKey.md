---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: D28EB28D-DBC6-48D5-AB0A-C56F56CD0104
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/set-azmediaservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaServiceKey.md
ms.openlocfilehash: 44c1ff2fe283e3cd804d20a8df21023b3c222150
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397456"
---
# <span data-ttu-id="6c22d-101">Set-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="6c22d-101">Set-AzMediaServiceKey</span></span>

## <span data-ttu-id="6c22d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6c22d-102">SYNOPSIS</span></span>
<span data-ttu-id="6c22d-103">Återskapar en nyckeln som används för att komma åt den REST-slutpunkt som är associerad med medie tjänsten.</span><span class="sxs-lookup"><span data-stu-id="6c22d-103">Regenerates a key used for accessing the REST endpoint associated with the media service.</span></span>

## <span data-ttu-id="6c22d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6c22d-104">SYNTAX</span></span>

```
Set-AzMediaServiceKey [-ResourceGroupName] <String> [-AccountName] <String> [-KeyType] <KeyType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c22d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6c22d-105">DESCRIPTION</span></span>
<span data-ttu-id="6c22d-106">Cmdleten **set-AzMediaServiceKey** återskapar en nyckeln som används för att öppna den ompresentations tillstånds överföring (rest) som är associerad med medie tjänsten.</span><span class="sxs-lookup"><span data-stu-id="6c22d-106">The **Set-AzMediaServiceKey** cmdlet regenerates a key used for accessing the Representational State Transfer (REST) endpoint associated with the media service.</span></span>

## <span data-ttu-id="6c22d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6c22d-107">EXAMPLES</span></span>

### <span data-ttu-id="6c22d-108">Exempel 1: återskapa den primära nyckeln som används för åtkomst till medie tjänsten</span><span class="sxs-lookup"><span data-stu-id="6c22d-108">Example 1: Regenerate the primary key used for accessing the Media Service</span></span>
```
PS C:\>Set-AzMediaServiceKey -ResourceGroupName "ResourceGroup004" -AccountName "MediaService001" -KeyType Primary
```

<span data-ttu-id="6c22d-109">Det här kommandot återskapar primär nyckeln för medie tjänsten som heter MediaService001 som tillhör resurs gruppen med namnet ResourceGroup004.</span><span class="sxs-lookup"><span data-stu-id="6c22d-109">This command regenerates the primary key for the media service named MediaService001 that belongs to the resource group named ResourceGroup004.</span></span>

### <span data-ttu-id="6c22d-110">Exempel 2: återskapa den sekundära nyckeln som används för åtkomst till medie tjänsten</span><span class="sxs-lookup"><span data-stu-id="6c22d-110">Example 2: Regenerates the secondary key used for accessing the Media Service</span></span>
```
PS C:\>Set-AzMediaServiceKey -ResourceGroupName "Resourcegroup123" -AccountName "MediaService002" -KeyType Secondary
```

<span data-ttu-id="6c22d-111">Det här kommandot återskapar den sekundära nyckeln för medie tjänsten som heter MediaService002 som tillhör resurs gruppen med namnet Resourcegroup123.</span><span class="sxs-lookup"><span data-stu-id="6c22d-111">This command regenerates the secondary key for the media service named MediaService002 that belongs to the resource group named Resourcegroup123.</span></span>

## <span data-ttu-id="6c22d-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6c22d-112">PARAMETERS</span></span>

### <span data-ttu-id="6c22d-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6c22d-113">-AccountName</span></span>
<span data-ttu-id="6c22d-114">Anger namnet på den medie tjänst som denna cmdlet ska återskapa.</span><span class="sxs-lookup"><span data-stu-id="6c22d-114">Specifies the name of the media service that this cmdlet regenerates.</span></span>

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

### <span data-ttu-id="6c22d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c22d-115">-DefaultProfile</span></span>
<span data-ttu-id="6c22d-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="6c22d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6c22d-117">-Värdetyp</span><span class="sxs-lookup"><span data-stu-id="6c22d-117">-KeyType</span></span>
<span data-ttu-id="6c22d-118">Anger medie tjänstens medietyp.</span><span class="sxs-lookup"><span data-stu-id="6c22d-118">Specifies the key type of the media service.</span></span>
<span data-ttu-id="6c22d-119">De acceptabla värdena för den här parametern är: primär eller sekundär.</span><span class="sxs-lookup"><span data-stu-id="6c22d-119">The acceptable values for this parameter are: Primary or Secondary.</span></span>

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

### <span data-ttu-id="6c22d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c22d-120">-ResourceGroupName</span></span>
<span data-ttu-id="6c22d-121">Anger namnet på den resurs grupp som innehåller medie tjänsten.</span><span class="sxs-lookup"><span data-stu-id="6c22d-121">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="6c22d-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6c22d-122">-Confirm</span></span>
<span data-ttu-id="6c22d-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6c22d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c22d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c22d-124">-WhatIf</span></span>
<span data-ttu-id="6c22d-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6c22d-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c22d-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6c22d-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c22d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c22d-127">CommonParameters</span></span>
<span data-ttu-id="6c22d-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c22d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c22d-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c22d-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c22d-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6c22d-130">INPUTS</span></span>

### <span data-ttu-id="6c22d-131">System. String</span><span class="sxs-lookup"><span data-stu-id="6c22d-131">System.String</span></span>

## <span data-ttu-id="6c22d-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6c22d-132">OUTPUTS</span></span>

### <span data-ttu-id="6c22d-133">Microsoft. Azure. commands. Media. Models. PSServiceKey</span><span class="sxs-lookup"><span data-stu-id="6c22d-133">Microsoft.Azure.Commands.Media.Models.PSServiceKey</span></span>

## <span data-ttu-id="6c22d-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6c22d-134">NOTES</span></span>

## <span data-ttu-id="6c22d-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6c22d-135">RELATED LINKS</span></span>

[<span data-ttu-id="6c22d-136">Get-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="6c22d-136">Get-AzMediaServiceKey</span></span>](./Get-AzMediaServiceKey.md)


