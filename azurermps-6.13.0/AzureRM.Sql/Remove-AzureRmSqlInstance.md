---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlmanagedinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlInstance.md
ms.openlocfilehash: 1da1c431d41c7277a8291bb9a012218057b9c678
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582540"
---
# <span data-ttu-id="6447a-101">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="6447a-101">Remove-AzureRmSqlInstance</span></span>

## <span data-ttu-id="6447a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6447a-102">SYNOPSIS</span></span>
<span data-ttu-id="6447a-103">Tar bort en Azure SQL-hanterad databas instans.</span><span class="sxs-lookup"><span data-stu-id="6447a-103">Removes an Azure SQL Managed Database Instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6447a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6447a-104">SYNTAX</span></span>

### <span data-ttu-id="6447a-105">RemoveInstanceFromInputParameters (standard)</span><span class="sxs-lookup"><span data-stu-id="6447a-105">RemoveInstanceFromInputParameters (Default)</span></span>
```
Remove-AzureRmSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6447a-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="6447a-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Remove-AzureRmSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6447a-107">RemoveInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="6447a-107">RemoveInstanceFromAzureResourceId</span></span>
```
Remove-AzureRmSqlInstance [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6447a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6447a-108">DESCRIPTION</span></span>
<span data-ttu-id="6447a-109">Cmdleten **Remove-AzureRmSqlInstance** tar bort en hanterad instans av en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="6447a-109">The **Remove-AzureRmSqlInstance** cmdlet removes an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="6447a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6447a-110">EXAMPLES</span></span>

### <span data-ttu-id="6447a-111">Exempel 1: ta bort instans</span><span class="sxs-lookup"><span data-stu-id="6447a-111">Example 1: Remove instance</span></span>
```
PS C:\>Remove-AzureRmSqlInstance -Name "managedInstance1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="6447a-112">Det här kommandot tar bort förekomsten med namnet managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="6447a-112">This command removes the instance named managedInstance1.</span></span>

## <span data-ttu-id="6447a-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6447a-113">PARAMETERS</span></span>

### <span data-ttu-id="6447a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6447a-114">-DefaultProfile</span></span>
<span data-ttu-id="6447a-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6447a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6447a-116">-Force</span><span class="sxs-lookup"><span data-stu-id="6447a-116">-Force</span></span>
<span data-ttu-id="6447a-117">Hoppa över bekräftelse meddelande för att utföra åtgärden</span><span class="sxs-lookup"><span data-stu-id="6447a-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="6447a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6447a-118">-InputObject</span></span>
<span data-ttu-id="6447a-119">AzureSqlManagedInstanceModel-objekt som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="6447a-119">The AzureSqlManagedInstanceModel object to remove</span></span>

```yaml
Type: AzureSqlManagedInstanceModel
Parameter Sets: RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: SqlInstance

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6447a-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="6447a-120">-Name</span></span>
<span data-ttu-id="6447a-121">SQL-instansnamn.</span><span class="sxs-lookup"><span data-stu-id="6447a-121">SQL instance name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveInstanceFromInputParameters
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6447a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6447a-122">-ResourceGroupName</span></span>
<span data-ttu-id="6447a-123">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="6447a-123">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveInstanceFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6447a-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6447a-124">-ResourceId</span></span>
<span data-ttu-id="6447a-125">Resurs-ID för instans objekt som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="6447a-125">The resource id of instance object to remove</span></span>

```yaml
Type: String
Parameter Sets: RemoveInstanceFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6447a-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6447a-126">-Confirm</span></span>
<span data-ttu-id="6447a-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6447a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6447a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6447a-128">-WhatIf</span></span>
<span data-ttu-id="6447a-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6447a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6447a-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6447a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6447a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6447a-131">CommonParameters</span></span>
<span data-ttu-id="6447a-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6447a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6447a-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6447a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6447a-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6447a-134">INPUTS</span></span>

### <span data-ttu-id="6447a-135">Microsoft. Azure. commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="6447a-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="6447a-136">System. String</span><span class="sxs-lookup"><span data-stu-id="6447a-136">System.String</span></span>

## <span data-ttu-id="6447a-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6447a-137">OUTPUTS</span></span>

### <span data-ttu-id="6447a-138">Microsoft. Azure. commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="6447a-138">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="6447a-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6447a-139">NOTES</span></span>

## <span data-ttu-id="6447a-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6447a-140">RELATED LINKS</span></span>
