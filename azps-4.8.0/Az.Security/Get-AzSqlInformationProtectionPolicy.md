---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSqlInformationProtectionPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSqlInformationProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSqlInformationProtectionPolicy.md
ms.openlocfilehash: 7f84c3b10577eea0d035c2ce84b3aa8a61af4a3d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94100862"
---
# <span data-ttu-id="b999a-101">Get-AzSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b999a-101">Get-AzSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="b999a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b999a-102">SYNOPSIS</span></span>
<span data-ttu-id="b999a-103">Hämtar den faktiska skydds principen för klient organisationens SQL information.</span><span class="sxs-lookup"><span data-stu-id="b999a-103">Retrieves the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="b999a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b999a-104">SYNTAX</span></span>

```
Get-AzSqlInformationProtectionPolicy [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b999a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b999a-105">DESCRIPTION</span></span>
<span data-ttu-id="b999a-106">Hämtar den faktiska skydds principen för klient organisationens SQL information.</span><span class="sxs-lookup"><span data-stu-id="b999a-106">Retrieves the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="b999a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b999a-107">EXAMPLES</span></span>

### <span data-ttu-id="b999a-108">Exempel</span><span class="sxs-lookup"><span data-stu-id="b999a-108">Example</span></span>
```powershell
PS C:\> Get-AzSqlInformationProtectionPolicy
```

## <span data-ttu-id="b999a-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b999a-109">PARAMETERS</span></span>

### <span data-ttu-id="b999a-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b999a-110">-AsJob</span></span>
<span data-ttu-id="b999a-111">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="b999a-111">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b999a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b999a-112">-DefaultProfile</span></span>
<span data-ttu-id="b999a-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b999a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b999a-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b999a-114">CommonParameters</span></span>
<span data-ttu-id="b999a-115">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b999a-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b999a-116">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b999a-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b999a-117">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b999a-117">INPUTS</span></span>

### <span data-ttu-id="b999a-118">System. String</span><span class="sxs-lookup"><span data-stu-id="b999a-118">System.string</span></span>

## <span data-ttu-id="b999a-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b999a-119">OUTPUTS</span></span>

### <span data-ttu-id="b999a-120">Microsoft. Azure. commands. SecurityCenter. Models. SqlInformationProtectionPolicy. PSSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b999a-120">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="b999a-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b999a-121">NOTES</span></span>

## <span data-ttu-id="b999a-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b999a-122">RELATED LINKS</span></span>