---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 388D4173-A937-42FA-81CB-C4A27F9D0B04
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADUser.md
ms.openlocfilehash: 9d65ed2f6bbc2e26c4e91916cc42bf2954c08252
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755425"
---
# <span data-ttu-id="7ab28-101">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="7ab28-101">Set-AzureRmADUser</span></span>

## <span data-ttu-id="7ab28-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7ab28-102">SYNOPSIS</span></span>
<span data-ttu-id="7ab28-103">Uppdaterar en befintlig Active Directory-användare.</span><span class="sxs-lookup"><span data-stu-id="7ab28-103">Updates an existing active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ab28-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7ab28-104">SYNTAX</span></span>

```
Set-AzureRmADUser -UPNOrObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <String>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ab28-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7ab28-105">DESCRIPTION</span></span>
<span data-ttu-id="7ab28-106">Uppdaterar en befintlig Active Directory-användare (arbets-eller skol konto som också kallas organisations-ID).</span><span class="sxs-lookup"><span data-stu-id="7ab28-106">Updates an existing active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="7ab28-107">Mer information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span><span class="sxs-lookup"><span data-stu-id="7ab28-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span></span>

## <span data-ttu-id="7ab28-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7ab28-108">EXAMPLES</span></span>

### <span data-ttu-id="7ab28-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7ab28-109">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="7ab28-110">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="7ab28-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="7ab28-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7ab28-111">PARAMETERS</span></span>

### <span data-ttu-id="7ab28-112">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7ab28-112">-DisplayName</span></span>
<span data-ttu-id="7ab28-113">Nytt namn som ska visas i adress boken för användaren.</span><span class="sxs-lookup"><span data-stu-id="7ab28-113">New name to display in the address book for the user.</span></span>
<span data-ttu-id="7ab28-114">Exempel-'Alex Wu ".</span><span class="sxs-lookup"><span data-stu-id="7ab28-114">Example-'Alex Wu'.</span></span>

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

### <span data-ttu-id="7ab28-115">-EnableAccount</span><span class="sxs-lookup"><span data-stu-id="7ab28-115">-EnableAccount</span></span>
<span data-ttu-id="7ab28-116">Sant för att aktivera kontot annars FALSE.</span><span class="sxs-lookup"><span data-stu-id="7ab28-116">True for enabling the account; otherwise, false.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ab28-117">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="7ab28-117">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="7ab28-118">Den får bara anges när du uppdaterar lösen ordet.</span><span class="sxs-lookup"><span data-stu-id="7ab28-118">It must be specified only when you are updating the password.</span></span>
<span data-ttu-id="7ab28-119">Annars kommer den att ignoreras.</span><span class="sxs-lookup"><span data-stu-id="7ab28-119">Otherwise it will be ignored.</span></span>
<span data-ttu-id="7ab28-120">Det måste anges om användaren måste ändra lösen ordet vid nästa lyckade inloggning (sant).</span><span class="sxs-lookup"><span data-stu-id="7ab28-120">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="7ab28-121">Standard beteende är (falskt) för att inte ändra lösen ordet vid nästa lyckade inloggning.</span><span class="sxs-lookup"><span data-stu-id="7ab28-121">Default behavior is (false) to not change the password on the next successful login.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ab28-122">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="7ab28-122">-Password</span></span>
<span data-ttu-id="7ab28-123">Nytt lösen ord för användaren.</span><span class="sxs-lookup"><span data-stu-id="7ab28-123">New password for the user.</span></span>
<span data-ttu-id="7ab28-124">Den måste uppfylla innehavarens komplexitets krav.</span><span class="sxs-lookup"><span data-stu-id="7ab28-124">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="7ab28-125">Vi rekommenderar att du anger ett starkt lösen ord.</span><span class="sxs-lookup"><span data-stu-id="7ab28-125">It is recommended to set a strong password.</span></span>

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

### <span data-ttu-id="7ab28-126">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="7ab28-126">-UPNOrObjectId</span></span>
<span data-ttu-id="7ab28-127">UPN-namnet (till exempel " someuser@contoso.com ) eller ObjectId för den användare som egenskaperna måste uppdateras för.</span><span class="sxs-lookup"><span data-stu-id="7ab28-127">The user principal name (e.g. 'someuser@contoso.com') or the objectId of the user for which the properties need to be updated.</span></span>

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

### <span data-ttu-id="7ab28-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7ab28-128">-Confirm</span></span>
<span data-ttu-id="7ab28-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7ab28-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ab28-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ab28-130">-WhatIf</span></span>
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

### <span data-ttu-id="7ab28-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ab28-131">-DefaultProfile</span></span>
<span data-ttu-id="7ab28-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7ab28-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ab28-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ab28-133">CommonParameters</span></span>
<span data-ttu-id="7ab28-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ab28-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ab28-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ab28-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ab28-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7ab28-136">INPUTS</span></span>

## <span data-ttu-id="7ab28-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7ab28-137">OUTPUTS</span></span>

### <span data-ttu-id="7ab28-138">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="7ab28-138">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="7ab28-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7ab28-139">NOTES</span></span>

## <span data-ttu-id="7ab28-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7ab28-140">RELATED LINKS</span></span>

[<span data-ttu-id="7ab28-141">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="7ab28-141">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="7ab28-142">New-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="7ab28-142">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="7ab28-143">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="7ab28-143">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)

