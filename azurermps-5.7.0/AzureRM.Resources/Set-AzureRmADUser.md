---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 388D4173-A937-42FA-81CB-C4A27F9D0B04
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADUser.md
ms.openlocfilehash: 325f134baf860b728aec3f144d9c9cf455c6b4ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573303"
---
# <span data-ttu-id="8593e-101">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="8593e-101">Set-AzureRmADUser</span></span>

## <span data-ttu-id="8593e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8593e-102">SYNOPSIS</span></span>
<span data-ttu-id="8593e-103">Uppdaterar en befintlig Active Directory-användare.</span><span class="sxs-lookup"><span data-stu-id="8593e-103">Updates an existing active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8593e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8593e-104">SYNTAX</span></span>

```
Set-AzureRmADUser -UPNOrObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8593e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8593e-105">DESCRIPTION</span></span>
<span data-ttu-id="8593e-106">Uppdaterar en befintlig Active Directory-användare (arbets-eller skol konto som också kallas organisations-ID).</span><span class="sxs-lookup"><span data-stu-id="8593e-106">Updates an existing active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="8593e-107">Mer information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span><span class="sxs-lookup"><span data-stu-id="8593e-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span></span>

## <span data-ttu-id="8593e-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8593e-108">EXAMPLES</span></span>

### <span data-ttu-id="8593e-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8593e-109">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="8593e-110">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="8593e-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="8593e-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8593e-111">PARAMETERS</span></span>

### <span data-ttu-id="8593e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8593e-112">-DefaultProfile</span></span>
<span data-ttu-id="8593e-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="8593e-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8593e-114">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8593e-114">-DisplayName</span></span>
<span data-ttu-id="8593e-115">Nytt namn som ska visas i adress boken för användaren.</span><span class="sxs-lookup"><span data-stu-id="8593e-115">New name to display in the address book for the user.</span></span>
<span data-ttu-id="8593e-116">Exempel-'Alex Wu ".</span><span class="sxs-lookup"><span data-stu-id="8593e-116">Example-'Alex Wu'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8593e-117">-EnableAccount</span><span class="sxs-lookup"><span data-stu-id="8593e-117">-EnableAccount</span></span>
<span data-ttu-id="8593e-118">Sant för att aktivera kontot annars FALSE.</span><span class="sxs-lookup"><span data-stu-id="8593e-118">True for enabling the account; otherwise, false.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8593e-119">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="8593e-119">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="8593e-120">Den får bara anges när du uppdaterar lösen ordet.</span><span class="sxs-lookup"><span data-stu-id="8593e-120">It must be specified only when you are updating the password.</span></span>
<span data-ttu-id="8593e-121">Annars kommer den att ignoreras.</span><span class="sxs-lookup"><span data-stu-id="8593e-121">Otherwise it will be ignored.</span></span>
<span data-ttu-id="8593e-122">Det måste anges om användaren måste ändra lösen ordet vid nästa lyckade inloggning (sant).</span><span class="sxs-lookup"><span data-stu-id="8593e-122">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="8593e-123">Standard beteende är (falskt) för att inte ändra lösen ordet vid nästa lyckade inloggning.</span><span class="sxs-lookup"><span data-stu-id="8593e-123">Default behavior is (false) to not change the password on the next successful login.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8593e-124">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="8593e-124">-Password</span></span>
<span data-ttu-id="8593e-125">Nytt lösen ord för användaren.</span><span class="sxs-lookup"><span data-stu-id="8593e-125">New password for the user.</span></span>
<span data-ttu-id="8593e-126">Den måste uppfylla innehavarens komplexitets krav.</span><span class="sxs-lookup"><span data-stu-id="8593e-126">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="8593e-127">Vi rekommenderar att du anger ett starkt lösen ord.</span><span class="sxs-lookup"><span data-stu-id="8593e-127">It is recommended to set a strong password.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8593e-128">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="8593e-128">-UPNOrObjectId</span></span>
<span data-ttu-id="8593e-129">UPN-namnet (till exempel " someuser@contoso.com ) eller ObjectId för den användare som egenskaperna måste uppdateras för.</span><span class="sxs-lookup"><span data-stu-id="8593e-129">The user principal name (e.g. 'someuser@contoso.com') or the objectId of the user for which the properties need to be updated.</span></span>

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

### <span data-ttu-id="8593e-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8593e-130">-Confirm</span></span>
<span data-ttu-id="8593e-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8593e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8593e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8593e-132">-WhatIf</span></span>
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

### <span data-ttu-id="8593e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8593e-133">CommonParameters</span></span>
<span data-ttu-id="8593e-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8593e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8593e-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8593e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8593e-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8593e-136">INPUTS</span></span>

### <span data-ttu-id="8593e-137">Ingen</span><span class="sxs-lookup"><span data-stu-id="8593e-137">None</span></span>
<span data-ttu-id="8593e-138">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="8593e-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8593e-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8593e-139">OUTPUTS</span></span>

### <span data-ttu-id="8593e-140">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="8593e-140">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="8593e-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8593e-141">NOTES</span></span>

## <span data-ttu-id="8593e-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8593e-142">RELATED LINKS</span></span>

[<span data-ttu-id="8593e-143">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="8593e-143">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="8593e-144">New-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="8593e-144">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="8593e-145">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="8593e-145">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)

