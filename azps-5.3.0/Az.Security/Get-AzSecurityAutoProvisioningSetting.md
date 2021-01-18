---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAutoProvisioningSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAutoProvisioningSetting.md
ms.openlocfilehash: 08631f5705a3a0255c42ac3d146cef45de1b4e56
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525656"
---
# <span data-ttu-id="90a98-101">Get-AzSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="90a98-101">Get-AzSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="90a98-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="90a98-102">SYNOPSIS</span></span>
<span data-ttu-id="90a98-103">Hämtar inställningar för automatisk konfiguration av säkerhet</span><span class="sxs-lookup"><span data-stu-id="90a98-103">Gets the security automatic provisioning settings</span></span>

## <span data-ttu-id="90a98-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="90a98-104">SYNTAX</span></span>

### <span data-ttu-id="90a98-105">SubscriptionScope (standard)</span><span class="sxs-lookup"><span data-stu-id="90a98-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAutoProvisioningSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90a98-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="90a98-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAutoProvisioningSetting -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="90a98-107">ID</span><span class="sxs-lookup"><span data-stu-id="90a98-107">ResourceId</span></span>
```
Get-AzSecurityAutoProvisioningSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="90a98-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="90a98-108">DESCRIPTION</span></span>
<span data-ttu-id="90a98-109">Med inställningarna för automatisk etablering kan du bestämma om du vill att Azure Security Center automatiskt ska tillhandahålla en säkerhets agent som installeras på din dator.</span><span class="sxs-lookup"><span data-stu-id="90a98-109">Automatic Provisioning Settings let you decide whether you want Azure Security Center to automatically provision a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="90a98-110">Säkerhets agenten övervakar din virtuella dator för att skapa säkerhets varningar och övervaka den virtuella datorns säkerhetskompatibilitet.</span><span class="sxs-lookup"><span data-stu-id="90a98-110">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="90a98-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="90a98-111">EXAMPLES</span></span>

### <span data-ttu-id="90a98-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="90a98-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="90a98-113">Hämtar inställningen för automatisk etablering för abonnemanget</span><span class="sxs-lookup"><span data-stu-id="90a98-113">Gets the auto provisioning setting for the subscription</span></span>

## <span data-ttu-id="90a98-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="90a98-114">PARAMETERS</span></span>

### <span data-ttu-id="90a98-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90a98-115">-DefaultProfile</span></span>
<span data-ttu-id="90a98-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="90a98-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90a98-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="90a98-117">-Name</span></span>
<span data-ttu-id="90a98-118">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="90a98-118">Resource name.</span></span>

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

### <span data-ttu-id="90a98-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="90a98-119">-ResourceId</span></span>
<span data-ttu-id="90a98-120">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="90a98-120">Resource ID.</span></span>

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

### <span data-ttu-id="90a98-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90a98-121">CommonParameters</span></span>
<span data-ttu-id="90a98-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90a98-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90a98-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="90a98-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90a98-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="90a98-124">INPUTS</span></span>

### <span data-ttu-id="90a98-125">System. String</span><span class="sxs-lookup"><span data-stu-id="90a98-125">System.String</span></span>

## <span data-ttu-id="90a98-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="90a98-126">OUTPUTS</span></span>

### <span data-ttu-id="90a98-127">Microsoft. Azure. commands. Security. Models. AutoProvisioningSettings. PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="90a98-127">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="90a98-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="90a98-128">NOTES</span></span>

## <span data-ttu-id="90a98-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="90a98-129">RELATED LINKS</span></span>
