---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/get-azdataboxcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxCredential.md
ms.openlocfilehash: 14ac010a912963ad1a41c2b47161d8598375968e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744829"
---
# <span data-ttu-id="ac8d7-101">Get-AzDataBoxCredential</span><span class="sxs-lookup"><span data-stu-id="ac8d7-101">Get-AzDataBoxCredential</span></span>

## <span data-ttu-id="ac8d7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ac8d7-102">SYNOPSIS</span></span>
<span data-ttu-id="ac8d7-103">Hämtar autentiseringsuppgifterna för data i ett visst jobb</span><span class="sxs-lookup"><span data-stu-id="ac8d7-103">Gets the databox credentials of a specific job</span></span>

## <span data-ttu-id="ac8d7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ac8d7-104">SYNTAX</span></span>

### <span data-ttu-id="ac8d7-105">GetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ac8d7-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzDataBoxCredential -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ac8d7-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac8d7-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac8d7-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ac8d7-107">DESCRIPTION</span></span>
<span data-ttu-id="ac8d7-108">Cmdleten **Get-AzDataBoxCredential** hämtar autentiseringsuppgifterna för data rutan för ett specifikt jobb.</span><span class="sxs-lookup"><span data-stu-id="ac8d7-108">The **Get-AzDataBoxCredential** cmdlet gets the credentials of the databox of a specific job.</span></span> <span data-ttu-id="ac8d7-109">De interna egenskaperna för det returnerade objektet är olika för olika SKU-typer.</span><span class="sxs-lookup"><span data-stu-id="ac8d7-109">The internal properties of the returned credentials object will be different for different Sku types.</span></span>

## <span data-ttu-id="ac8d7-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ac8d7-110">EXAMPLES</span></span>

### <span data-ttu-id="ac8d7-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ac8d7-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxCredential -ResourceGroupName TestRg1 -Name TestJob1

JobName     JobSecrets
-------     ----------
TestJob1    Microsoft.Azure.Management.DataBox.Models.DataboxJobSecrets
```

<span data-ttu-id="ac8d7-112">Det här retuns JobSecrets för det angivna jobbet</span><span class="sxs-lookup"><span data-stu-id="ac8d7-112">This retuns the JobSecrets of the specified job</span></span>

### <span data-ttu-id="ac8d7-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="ac8d7-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxCredential -ResourceId "/subscriptions/fa68082f-8ff7-4a25-95c7-ce9da541242f/resourceGroups/TestRg1/providers/Microsoft.DataBox/jobs/TestJob1"

JobName     JobSecrets
-------     ----------
TestJob1    Microsoft.Azure.Management.DataBox.Models.DataboxJobSecrets
```

<span data-ttu-id="ac8d7-114">Det här retuns JobSecrets för det angivna jobbet</span><span class="sxs-lookup"><span data-stu-id="ac8d7-114">This retuns the JobSecrets of the specified job</span></span>

## <span data-ttu-id="ac8d7-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ac8d7-115">PARAMETERS</span></span>

### <span data-ttu-id="ac8d7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac8d7-116">-DefaultProfile</span></span>
<span data-ttu-id="ac8d7-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ac8d7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac8d7-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="ac8d7-118">-Name</span></span>
<span data-ttu-id="ac8d7-119">Jobbnamn</span><span class="sxs-lookup"><span data-stu-id="ac8d7-119">Databox Job Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac8d7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac8d7-120">-ResourceGroupName</span></span>
<span data-ttu-id="ac8d7-121">Namn på jobb i en datastapel</span><span class="sxs-lookup"><span data-stu-id="ac8d7-121">Databox Job Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac8d7-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ac8d7-122">-ResourceId</span></span>
<span data-ttu-id="ac8d7-123">Resurs-ID för datastapel</span><span class="sxs-lookup"><span data-stu-id="ac8d7-123">Databox Job Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac8d7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac8d7-124">CommonParameters</span></span>
<span data-ttu-id="ac8d7-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac8d7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac8d7-126">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ac8d7-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac8d7-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ac8d7-127">INPUTS</span></span>

### <span data-ttu-id="ac8d7-128">System. String</span><span class="sxs-lookup"><span data-stu-id="ac8d7-128">System.String</span></span>

## <span data-ttu-id="ac8d7-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ac8d7-129">OUTPUTS</span></span>

### <span data-ttu-id="ac8d7-130">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Management. data. UnencryptedCredentials, Microsoft. Azure. Management. data, version = 1.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="ac8d7-130">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Management.DataBox.Models.UnencryptedCredentials, Microsoft.Azure.Management.DataBox, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="ac8d7-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ac8d7-131">NOTES</span></span>

## <span data-ttu-id="ac8d7-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ac8d7-132">RELATED LINKS</span></span>