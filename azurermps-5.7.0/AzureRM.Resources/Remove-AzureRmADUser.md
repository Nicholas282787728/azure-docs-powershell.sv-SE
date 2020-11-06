---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 9F9B2691-BB3F-4644-BD95-6D74777D1E99
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADUser.md
ms.openlocfilehash: 735ea22547183b8047a3a32d0a147b428b39f630
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583059"
---
# <span data-ttu-id="54a77-101">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="54a77-101">Remove-AzureRmADUser</span></span>

## <span data-ttu-id="54a77-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="54a77-102">SYNOPSIS</span></span>
<span data-ttu-id="54a77-103">Tar bort en Active Directory-användare.</span><span class="sxs-lookup"><span data-stu-id="54a77-103">Deletes an active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54a77-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="54a77-104">SYNTAX</span></span>

```
Remove-AzureRmADUser -UPNOrObjectId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54a77-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="54a77-105">DESCRIPTION</span></span>
<span data-ttu-id="54a77-106">Tar bort en Active Directory-användare (arbets-eller skol konto som också kallas organisations-ID).</span><span class="sxs-lookup"><span data-stu-id="54a77-106">Deletes an active directory user (work/school account also popularly known as org-id).</span></span>

## <span data-ttu-id="54a77-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="54a77-107">EXAMPLES</span></span>

### <span data-ttu-id="54a77-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="54a77-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="54a77-109">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="54a77-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="54a77-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="54a77-110">PARAMETERS</span></span>

### <span data-ttu-id="54a77-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54a77-111">-DefaultProfile</span></span>
<span data-ttu-id="54a77-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="54a77-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="54a77-113">-Force</span><span class="sxs-lookup"><span data-stu-id="54a77-113">-Force</span></span>
<span data-ttu-id="54a77-114">Om det anges ber vi dig att bekräfta borttagning av användare.</span><span class="sxs-lookup"><span data-stu-id="54a77-114">If specified, doesn't ask for confirmation for deleting user.</span></span>

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

### <span data-ttu-id="54a77-115">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="54a77-115">-UPNOrObjectId</span></span>
<span data-ttu-id="54a77-116">Användarens huvud namn eller objectId för den användare som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="54a77-116">The user principal name or the objectId of the user to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54a77-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="54a77-117">-Confirm</span></span>
<span data-ttu-id="54a77-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="54a77-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54a77-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54a77-119">-WhatIf</span></span>
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

### <span data-ttu-id="54a77-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54a77-120">CommonParameters</span></span>
<span data-ttu-id="54a77-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54a77-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54a77-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54a77-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54a77-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="54a77-123">INPUTS</span></span>

### <span data-ttu-id="54a77-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="54a77-124">None</span></span>
<span data-ttu-id="54a77-125">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="54a77-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="54a77-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="54a77-126">OUTPUTS</span></span>

## <span data-ttu-id="54a77-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="54a77-127">NOTES</span></span>

## <span data-ttu-id="54a77-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="54a77-128">RELATED LINKS</span></span>

[<span data-ttu-id="54a77-129">New-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="54a77-129">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="54a77-130">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="54a77-130">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="54a77-131">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="54a77-131">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

