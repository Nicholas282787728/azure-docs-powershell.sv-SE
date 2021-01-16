---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafPolicy.md
ms.openlocfilehash: ea1ace189271c96bbf4bda0bc67385c678ef3c40
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98404611"
---
# <span data-ttu-id="4616c-101">Get-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="4616c-101">Get-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="4616c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4616c-102">SYNOPSIS</span></span>
<span data-ttu-id="4616c-103">Skaffa WAF policy</span><span class="sxs-lookup"><span data-stu-id="4616c-103">Get WAF policy</span></span>

## <span data-ttu-id="4616c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4616c-104">SYNTAX</span></span>

```
Get-AzFrontDoorWafPolicy -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4616c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4616c-105">DESCRIPTION</span></span>
<span data-ttu-id="4616c-106">Funktionen **Get-AzFrontDoorWafPolicy** CMDLETGET får WAF policy i en resurs grupp under den aktuella prenumerationen</span><span class="sxs-lookup"><span data-stu-id="4616c-106">The **Get-AzFrontDoorWafPolicy** cmdletGet gets WAF policy in a resource group under the current subscription</span></span>

## <span data-ttu-id="4616c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4616c-107">EXAMPLES</span></span>

### <span data-ttu-id="4616c-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4616c-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="4616c-109">Skaffa en WAF policy med namnet $policyName i $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4616c-109">Get a WAF policy called $policyName in $resourceGroupName</span></span>

### <span data-ttu-id="4616c-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="4616c-110">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention           Disabled
{policyName} Detection             Enabled                           403 https://www.bing.com/
{policyName} Detection             Enabled                           404
```

<span data-ttu-id="4616c-111">Hämta alla WAF-principer i $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4616c-111">Get all WAF policy in $resourceGroupName</span></span>

## <span data-ttu-id="4616c-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4616c-112">PARAMETERS</span></span>

### <span data-ttu-id="4616c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4616c-113">-DefaultProfile</span></span>
<span data-ttu-id="4616c-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4616c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4616c-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="4616c-115">-Name</span></span>
<span data-ttu-id="4616c-116">FireWallPolicy namn.</span><span class="sxs-lookup"><span data-stu-id="4616c-116">FireWallPolicy name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4616c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4616c-117">-ResourceGroupName</span></span>
<span data-ttu-id="4616c-118">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="4616c-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4616c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4616c-119">CommonParameters</span></span>
<span data-ttu-id="4616c-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4616c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4616c-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4616c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4616c-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4616c-122">INPUTS</span></span>

### <span data-ttu-id="4616c-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="4616c-123">None</span></span>

## <span data-ttu-id="4616c-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4616c-124">OUTPUTS</span></span>

### <span data-ttu-id="4616c-125">Microsoft. Azure. commands. FrontDoor. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="4616c-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="4616c-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4616c-126">NOTES</span></span>

## <span data-ttu-id="4616c-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4616c-127">RELATED LINKS</span></span>

<span data-ttu-id="4616c-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md) 
 [Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="4616c-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)
[Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)</span></span>
