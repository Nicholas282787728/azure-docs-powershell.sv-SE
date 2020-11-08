---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySetting.md
ms.openlocfilehash: 708fb6b3807e874d00c3e555ef84973572edcd1c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269107"
---
# <span data-ttu-id="59c85-101">Get-AzSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="59c85-101">Get-AzSecuritySetting</span></span>

## <span data-ttu-id="59c85-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="59c85-102">SYNOPSIS</span></span>
<span data-ttu-id="59c85-103">Hämta säkerhets inställningar i Azure Security Center</span><span class="sxs-lookup"><span data-stu-id="59c85-103">Get security settings in Azure Security Center</span></span>

## <span data-ttu-id="59c85-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="59c85-104">SYNTAX</span></span>

### <span data-ttu-id="59c85-105">SubscriptionScope (standard)</span><span class="sxs-lookup"><span data-stu-id="59c85-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59c85-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="59c85-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySetting -SettingName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59c85-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="59c85-107">DESCRIPTION</span></span>
<span data-ttu-id="59c85-108">Get-AzSecuritySetting cmdlet får säkerhets inställningar i Azure Security Center.</span><span class="sxs-lookup"><span data-stu-id="59c85-108">The Get-AzSecuritySetting cmdlet get security settings in Azure Security Center.</span></span>

## <span data-ttu-id="59c85-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="59c85-109">EXAMPLES</span></span>

### <span data-ttu-id="59c85-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="59c85-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSecuritySetting -SettingName "MCAS"

Id: "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/settings/MCAS"
Name: "MCAS"
Type: "Microsoft.Security/settings"
Enabled: true
```

<span data-ttu-id="59c85-111">Hämtar en inställning för data export för MCAS</span><span class="sxs-lookup"><span data-stu-id="59c85-111">Gets an MCAS data export setting</span></span>   

## <span data-ttu-id="59c85-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="59c85-112">PARAMETERS</span></span>

### <span data-ttu-id="59c85-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59c85-113">-DefaultProfile</span></span>
<span data-ttu-id="59c85-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="59c85-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59c85-115">-SettingName</span><span class="sxs-lookup"><span data-stu-id="59c85-115">-SettingName</span></span>
<span data-ttu-id="59c85-116">Ange namn.</span><span class="sxs-lookup"><span data-stu-id="59c85-116">Setting name.</span></span> <span data-ttu-id="59c85-117">(MCAS/WDATP)</span><span class="sxs-lookup"><span data-stu-id="59c85-117">(MCAS/WDATP)</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59c85-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59c85-118">CommonParameters</span></span>
<span data-ttu-id="59c85-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59c85-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59c85-120">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="59c85-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59c85-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="59c85-121">INPUTS</span></span>

### <span data-ttu-id="59c85-122">System. String</span><span class="sxs-lookup"><span data-stu-id="59c85-122">System.String</span></span>

## <span data-ttu-id="59c85-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="59c85-123">OUTPUTS</span></span>

### <span data-ttu-id="59c85-124">Microsoft. Azure. commands. Security. Models. Settings. PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="59c85-124">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="59c85-125">Microsoft. Azure. commands. Security. Models. Settings. PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="59c85-125">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

## <span data-ttu-id="59c85-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="59c85-126">NOTES</span></span>

## <span data-ttu-id="59c85-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="59c85-127">RELATED LINKS</span></span>
