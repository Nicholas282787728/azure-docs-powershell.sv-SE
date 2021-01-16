---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azsqlvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMConfig.md
ms.openlocfilehash: 0f914ab2f5c39cd53239302b2f0acd12a3e13133
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394091"
---
# <span data-ttu-id="c748a-101">New-AzSqlVMConfig</span><span class="sxs-lookup"><span data-stu-id="c748a-101">New-AzSqlVMConfig</span></span>

## <span data-ttu-id="c748a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c748a-102">SYNOPSIS</span></span>
<span data-ttu-id="c748a-103">Skapar en ny konfiguration för en virtuell SQL-dator.</span><span class="sxs-lookup"><span data-stu-id="c748a-103">Creates a new configuration for a sql virtual machine.</span></span>

## <span data-ttu-id="c748a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c748a-104">SYNTAX</span></span>

```
New-AzSqlVMConfig [-LicenseType] <String> [-Offer <String>] [-Sku <String>] [-SqlManagementType <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c748a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c748a-105">DESCRIPTION</span></span>
<span data-ttu-id="c748a-106">New-AzSqlVMConfig-cmdleten skapar ett nytt konfigurations objekt för en virtuell SQL-dator.</span><span class="sxs-lookup"><span data-stu-id="c748a-106">The New-AzSqlVMConfig cmdlet creates a new configuration object for a sql virtual machine.</span></span>

## <span data-ttu-id="c748a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c748a-107">EXAMPLES</span></span>

### <span data-ttu-id="c748a-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c748a-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzSqlVMConfig -LicenseType "PAYG"
PS C:\> New-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm" -SqlVM $config
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="c748a-109">Skapar ett lokalt konfigurerbart objekt av SQL Virtual Machine som kan användas för att skapa en virtuell Azure SQL-dator.</span><span class="sxs-lookup"><span data-stu-id="c748a-109">Creates a local configurable object of sql virtual machine that can be used in order to create an Azure sql virtual machine.</span></span>

## <span data-ttu-id="c748a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c748a-110">PARAMETERS</span></span>

### <span data-ttu-id="c748a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c748a-111">-DefaultProfile</span></span>
<span data-ttu-id="c748a-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c748a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c748a-113">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="c748a-113">-LicenseType</span></span>
<span data-ttu-id="c748a-114">Licens typ för SQL Virtual Machine.</span><span class="sxs-lookup"><span data-stu-id="c748a-114">SQL virtual machine license type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c748a-115">-Ge</span><span class="sxs-lookup"><span data-stu-id="c748a-115">-Offer</span></span>
<span data-ttu-id="c748a-116">Utbud av virtuell SQL-dator.</span><span class="sxs-lookup"><span data-stu-id="c748a-116">SQL virtual machine offer.</span></span>

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

### <span data-ttu-id="c748a-117">-SKU</span><span class="sxs-lookup"><span data-stu-id="c748a-117">-Sku</span></span>
<span data-ttu-id="c748a-118">Typ av SQL Virtual Machine-version.</span><span class="sxs-lookup"><span data-stu-id="c748a-118">SQL virtual machine edition type.</span></span>

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

### <span data-ttu-id="c748a-119">-SqlManagementType</span><span class="sxs-lookup"><span data-stu-id="c748a-119">-SqlManagementType</span></span>
<span data-ttu-id="c748a-120">Hanterings typ för SQL virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="c748a-120">SQL virtual machine management type.</span></span>

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

### <span data-ttu-id="c748a-121">-Tagg</span><span class="sxs-lookup"><span data-stu-id="c748a-121">-Tag</span></span>
<span data-ttu-id="c748a-122">De taggar som ska kopplas till den virtuella SQL-datorn</span><span class="sxs-lookup"><span data-stu-id="c748a-122">The tags to associate with the SQL virtual machine</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c748a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c748a-123">CommonParameters</span></span>
<span data-ttu-id="c748a-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c748a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c748a-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c748a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c748a-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c748a-126">INPUTS</span></span>

### <span data-ttu-id="c748a-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="c748a-127">None</span></span>

## <span data-ttu-id="c748a-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c748a-128">OUTPUTS</span></span>

### <span data-ttu-id="c748a-129">Microsoft. Azure. commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="c748a-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="c748a-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c748a-130">NOTES</span></span>

## <span data-ttu-id="c748a-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c748a-131">RELATED LINKS</span></span>
